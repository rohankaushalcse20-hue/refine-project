---
title: Content सुरक्षित करना
---

import { Sandpack, CreateAuthProviderFile, AddAuthProviderToAppTsx, AddCheckMethodToAuthProvider, AddAuthenticatedComponentToAppTsx } from "./sandpack.tsx";

<Sandpack>

इस चरण में हम `check` method के साथ एक basic `authProvider` implement करेंगे, ताकि user की authentication status validate हो सके और unauthenticated users से content सुरक्षित रखा जा सके।

Refine अपने आसान `authProvider` interface की वजह से किसी भी authentication solution के साथ काम कर सकता है। हम अपनी fake REST API के लिए implementation set up करेंगे, जो simple authentication endpoints भी देती है।

Supported auth providers के बारे में अधिक जानने के लिए Authentication guide का [Supported Authentication Providers](/core/docs/guides-concepts/authentication/#supported-auth-providers) section देखें।

## Auth Provider बनाना

हम हर method को एक-एक करके implement करेंगे, ताकि सभी details ठीक से cover हों।

सबसे पहले, हम अपने project में `src/providers/auth-provider.ts` file बनाएंगे। इसी file में वे सभी methods होंगे जिन्हें हमें अपने auth provider के लिए implement करना है।

<CreateAuthProviderFile />

इसके बाद, हम `src/App.tsx` file में `authProvider` prop के जरिए अपना auth provider `<Refine />` component को pass करेंगे।

नीचे दी गई lines जोड़कर अपनी `src/App.tsx` file update करें:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
// highlight-next-line
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

export default function App(): JSX.Element {
  return (
    <Refine
      dataProvider={dataProvider}
      // highlight-next-line
      authProvider={authProvider}
    >
      {/* <ShowProduct /> */}
      {/* <EditProduct /> */}
      <ListProducts />
      {/* <CreateProduct /> */}
    </Refine>
  );
}
```

<AddAuthProviderToAppTsx />

## `check` method implement करना

`check` method का उपयोग `useIsAuthenticated` hook और `<Authenticated />` component user की authentication status check करने के लिए करते हैं। इसे एक `Promise` return करना चाहिए जो एक object में resolve हो।

अगर user authenticated है, तो object में `authenticated: true` property होनी चाहिए। अन्यथा उसमें `authenticated: false` property होनी चाहिए।

हम अपनी API के `login` method से access token प्राप्त करेंगे और उसे local storage में store करेंगे। अब देखते हैं कि token local storage में मौजूद है या नहीं।

नीचे दी गई lines जोड़कर अपनी `src/providers/auth-provider.ts` file update करें:

```ts title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  // highlight-start
  check: async () => {
    // When logging in, we'll obtain an access token from our API and store it in the local storage.
    // Now let's check if the token exists in the local storage.
    // In the later steps, we'll be implementing the `login` and `logout` methods.
    const token = localStorage.getItem("my_access_token");

    return { authenticated: Boolean(token) };
  },
  // highlight-end
  login: async ({ email, password }) => {
    throw new Error("Not implemented");
  },
  logout: async () => {
    throw new Error("Not implemented");
  },
  onError: async (error) => {
    throw new Error("Not implemented");
  },
  // ...
};
```

<AddCheckMethodToAuthProvider />

## `<Authenticated />` component का उपयोग

`check` method implement करने के बाद हम unauthenticated users से अपना content सुरक्षित रखने के लिए `<Authenticated />` component का उपयोग कर पाएंगे।

चलिए `src/App.tsx` file में `<Authenticated />` component जोड़ते हैं और `<Refine />` component के अंदर अपने content को इससे wrap करते हैं।

नीचे दी गई lines जोड़कर अपनी `src/App.tsx` file update करें:

```tsx title="src/App.tsx"
// highlight-next-line
import { Refine, Authenticated } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider} authProvider={authProvider}>
      {/* highlight-start */}
      <Authenticated key="protected" fallback={<div>Not authenticated</div>}>
        {/* <ShowProduct /> */}
        {/* <EditProduct /> */}
        <ListProducts />
        {/* <CreateProduct /> */}
      </Authenticated>
      {/* highlight-end */}
    </Refine>
  );
}
```

<AddAuthenticatedComponentToAppTsx />

:::note

ध्यान दें कि हमने `<Authenticated />` component में `key` prop जोड़ा है। Component के सही तरीके से काम करने के लिए यह जरूरी है, खासकर जब इसे उसी render tree में कई बार उपयोग किया जाता है।

:::

अब आपको `<Authenticated />` component action में दिखना चाहिए। हमारा content render नहीं होगा और उसकी जगह `fallback` prop render होगा।

:::tip

आप चाहें तो `useIsAuthenticated` hook का भी उपयोग कर सकते हैं, जिसे `<Authenticated />` component internally use करता है। इसके बारे में आप [useIsAuthenticated](/core/docs/authentication/hooks/use-is-authenticated/) hook documentation में अधिक सीख सकते हैं।

:::

अगले चरण में हम login और logout functionality implement करेंगे और अपने `check` method को सही तरीके से काम करने योग्य बनाएंगे।

</Sandpack>
