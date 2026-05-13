---
title: Record update करना
---

import { Sandpack, AddUpdateMethod, CreateEditProductFile, AddUseUpdateToEditProduct, AddEditProductToAppTsx } from "./sandpack.tsx";

<Sandpack>

इस चरण में हम API में record update करने के लिए Refine के `useUpdate` hook के बारे में सीखेंगे और अपने data provider में `update` method implement करेंगे।

## `update` method implement करना

Refine hooks से record update करने के लिए सबसे पहले हमें अपने data provider में [`update`](/core/docs/data/data-provider/#update-) method implement करना होगा। जब हम अपने components में [`useUpdate`](/core/docs/data/hooks/use-update) hook या उसके extensions का उपयोग करते हैं, तब यह method call होगा।

`update` method `resource`, `id`, `variables` और `meta` properties स्वीकार करता है।

- `resource` उस entity को दर्शाता है जिसे हम update कर रहे हैं
- `id` उस record की ID है जिसे हम update कर रहे हैं
- `variables` वह object है जिसमें API को भेजा जाने वाला data होता है।
- `meta` hook को pass की गई किसी भी अतिरिक्त data वाली object है।

हमारी fake API की `products` entity `/products/:id` endpoint पर `PATCH` request के साथ record update करने की अपेक्षा करती है। इसलिए request बनाने के लिए हम `resource`, `id` और `variables` properties का उपयोग करेंगे।

नीचे दी गई lines जोड़कर अपनी `src/providers/data-provider.ts` file update करें:

```ts title="src/providers/data-provider.ts"
import type { DataProvider } from "@refinedev/core";

const API_URL = "https://api.fake-rest.refine.dev";

export const dataProvider: DataProvider = {
  getOne: async ({ resource, id, meta }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`);

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-start
  update: async ({ resource, id, variables }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`, {
      method: "PATCH",
      body: JSON.stringify(variables),
      headers: {
        "Content-Type": "application/json",
      },
    });

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-end
  getList: () => {
    throw new Error("Not implemented");
  },
  /* ... */
};
```

<AddUpdateMethod />

## `useUpdate` hook का उपयोग

`update` method implement करने के बाद हम `useUpdate` hook call कर पाएंगे और अपनी API में single record update कर पाएंगे। चलिए `EditProduct` नाम का component बनाते हैं और उसे अपने `<Refine />` component के अंदर mount करते हैं।

<CreateEditProductFile />

शुरुआत में हम `EditProduct` component में `useOne` hook call शामिल करेंगे, ताकि जिस record को update करना है उसे fetch किया जा सके।

फिर हम `EditProduct` के अंदर `useUpdate` hook का उपयोग करके API में `products` entity का single record update करेंगे।

नीचे दी गई lines जोड़कर अपनी `src/pages/products/edit.tsx` file update करें:

```tsx title="src/pages/products/edit.tsx"
// highlight-next-line
import { useOne, useUpdate } from "@refinedev/core";

export const EditProduct = () => {
  const {
    result,
    query: { isLoading },
  } = useOne({ resource: "products", id: 123 });
  // highlight-next-line
  const {
    mutate,
    mutation: { isPending: isUpdating },
  } = useUpdate();

  if (isLoading) {
    return <div>Loading...</div>;
  }

  const updatePrice = async () => {
    // highlight-start
    await mutate({
      resource: "products",
      id: 123,
      values: {
        price: Math.floor(Math.random() * 100),
      },
    });
    // highlight-end
  };

  return (
    <div>
      <div>Product name: {result?.name}</div>
      <div>Product price: ${result?.price}</div>
      <button onClick={updatePrice}>Update Price</button>
    </div>
  );
};
```

<AddUseUpdateToEditProduct />

अंत में, हम `EditProduct` component को अपने `<Refine />` component के अंदर mount करेंगे।

नीचे दी गई lines जोड़कर अपनी `src/App.tsx` file update करें:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";

import { ShowProduct } from "./pages/products/show";
// highlight-next-line
import { EditProduct } from "./pages/products/edit";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider}>
      {/* <ShowProduct /> */}
      {/* highlight-next-line */}
      <EditProduct />
    </Refine>
  );
}
```

<AddEditProductToAppTsx />

अब screen पर product name और price दोनों दिखने चाहिए। जब आप `Update Price` button पर click करेंगे, तो product की price update हो जाएगी।

:::tip Smart Invalidations

ध्यान दें कि जब हम `useUpdate` से price update करते हैं, तो पहले call किया गया `useOne` hook अपने आप invalidated हो जाता है। ऐसा इसलिए है क्योंकि Refine record update होने पर उसी resource और id का उपयोग करने वाली सभी queries invalidate करता है। इससे screen पर हमेशा latest data दिखता है और हमें queries manually invalidate नहीं करनी पड़तीं।

:::

अगले चरण में हम API से records की list fetch करने के लिए Refine के `useList` hook के बारे में सीखेंगे और अपने data provider में `getList` method implement करेंगे।

</Sandpack>
