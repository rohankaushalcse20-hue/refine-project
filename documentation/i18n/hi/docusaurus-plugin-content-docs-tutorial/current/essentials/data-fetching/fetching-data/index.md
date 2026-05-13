---
title: Record fetch करना
---

import { Sandpack, AddGetOneMethod, CreateShowProductFile, AddUseOneToShowProduct, AddShowProductToAppTsx } from "./sandpack.tsx";

<Sandpack>

इस चरण में हम API से single record fetch करने के लिए Refine के `useOne` hook के बारे में सीखेंगे और अपने data provider में `getOne` method implement करेंगे।

## `getOne` method implement करना

Refine hooks से record fetch करने के लिए सबसे पहले हमें अपने data provider में [`getOne`](/core/docs/data/data-provider/#getone-) method implement करना होगा। जब हम अपने components में [`useOne`](/core/docs/data/hooks/use-one) hook या उसके extensions का उपयोग करते हैं, तब यह method call होगा।

`getOne` method `resource`, `id` और `meta` properties स्वीकार करता है।

- `resource` उस entity को दर्शाता है जिसे हम fetch कर रहे हैं।
- `id` उस record की ID है जिसे हम fetch कर रहे हैं।
- `meta` hook को pass की गई किसी भी अतिरिक्त data वाली object है।

हमारी fake API में `products` entity है और वह `/products/:id` endpoint के जरिए single record fetch करने की अपेक्षा करती है। इसलिए request बनाने के लिए हम `resource` और `id` properties का उपयोग करेंगे।

नीचे दी गई lines जोड़कर अपनी `src/providers/data-provider.ts` file update करें:

```ts title="src/providers/data-provider.ts"
import type { DataProvider } from "@refinedev/core";

const API_URL = "https://api.fake-rest.refine.dev";

export const dataProvider: DataProvider = {
  // highlight-start
  getOne: async ({ resource, id, meta }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`);

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-end
  update: () => {
    throw new Error("Not implemented");
  },
  getList: () => {
    throw new Error("Not implemented");
  },
  /* ... */
};
```

<AddGetOneMethod />

## `useOne` hook का उपयोग

`getOne` method implement करने के बाद हम `useOne` hook call कर पाएंगे और अपनी API से single record fetch कर पाएंगे। चलिए `ShowProduct` नाम का component बनाते हैं और उसे अपने `<Refine />` component के अंदर mount करते हैं।

<CreateShowProductFile />

इसके बाद, हम `useOne` hook import करेंगे और उसे अपने `ShowProduct` component के अंदर उपयोग करके API से `products` entity का एक single record fetch करेंगे।

नीचे दी गई lines जोड़कर अपनी `src/pages/products/show.tsx` file update करें:

```tsx title="src/pages/products/show.tsx"
// highlight-next-line
import { useOne } from "@refinedev/core";

export const ShowProduct = () => {
  // highlight-next-line
  const {
    result,
    query: { isLoading },
  } = useOne({ resource: "products", id: 123 });

  if (isLoading) {
    return <div>Loading...</div>;
  }

  return <div>Product name: {result?.name}</div>;
};
```

<AddUseOneToShowProduct />

अंत में, हम `ShowProduct` component को अपने `<Refine />` component के अंदर mount करेंगे।

नीचे दी गई lines जोड़कर अपनी `src/App.tsx` file update करें:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
// highlight-next-line
import { ShowProduct } from "./pages/products/show";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider}>
      {/* highlight-next-line */}
      <ShowProduct />
    </Refine>
  );
}
```

<AddShowProductToAppTsx />

अब screen पर product name दिखना चाहिए।

अगले चरण में हम API से single record update करने के लिए Refine के `useUpdate` hook के बारे में सीखेंगे और अपने data provider में `update` method implement करेंगे।

</Sandpack>
