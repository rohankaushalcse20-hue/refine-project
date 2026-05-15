---
title: User Identity का उपयोग
---

import { Sandpack, AddGetIdentityMethodToAuthProvider, AddUseGetIdentityToHeaderComponent } from "./sandpack.tsx";

<Sandpack>

पिछले चरणों में हमने login और logout functionality जोड़ी और unauthenticated users से अपना content सुरक्षित किया। अब हम सीखेंगे कि अपनी API से user identity पाने के लिए Refine के `useGetIdentity` hook का उपयोग कैसे करें और अपने auth provider में `getIdentity` method कैसे implement करें।

हम user को welcome message दिखाने के लिए `UserGreeting` नाम का एक सरल component implement करेंगे।

## `getIdentity` Method Implement करना

`getIdentity` method हमारी API से user की identity लाने के लिए उपयोग होता है। इसे एक ऐसी `Promise` return करनी चाहिए जो object में resolve हो। उस object में user की identity होनी चाहिए।

हमारी fake REST API को `/auth/me` endpoint पर `GET` request चाहिए, जिसमें `Authorization` header में `token` भेजा जाता है। response body में user की identity return होगी।

अपने `src/providers/auth-provider.ts` file में ये lines जोड़कर update करें:

```ts title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  // highlight-start
  getIdentity: async () => {
    const response = await fetch("https://api.fake-rest.refine.dev/auth/me", {
      headers: {
        Authorization: localStorage.getItem("my_access_token"),
      },
    });

    if (response.status < 200 || response.status > 299) {
      return null;
    }

    const data = await response.json();

    return data;
  },
  // highlight-end
  logout: async () => {
    /* ... */
  },
  login: async ({ email, password }) => {
    /* ... */
  },
  check: async () => {
    /* ... */
  },
  onError: async (error) => {
    /* ... */
  },
  // ...
};
```

<AddGetIdentityMethodToAuthProvider />

## `useGetIdentity` Hook का उपयोग

`getIdentity` method implement करने के बाद हम `useGetIdentity` hook call कर पाएंगे और अपनी API से user की identity प्राप्त कर पाएंगे।

अब हम user को greet करने के लिए अपने `<Header />` component के अंदर `useGetIdentity` hook का उपयोग करेंगे।

अपने `src/components/header.tsx` file में ये lines जोड़कर update करें:

```tsx title="src/components/header.tsx"
import React from "react";
import { useLogout, useGetIdentity } from "@refinedev/core";

export const Header = () => {
  const { mutate, isPending } = useLogout();
  const { data: identity } = useGetIdentity();

  return (
    <>
      <h2>
        <span>Welcome, </span>
        <span>{identity?.name ?? ""}</span>
      </h2>
      <button type="button" disabled={isPending} onClick={mutate}>
        Logout
      </button>
    </>
  );
};
```

<AddUseGetIdentityToHeaderComponent />

अब जब हम login करेंगे, तो screen पर user name के साथ welcome message दिखना चाहिए।

:::simple Note

Demonstration के उद्देश्य से हमारी fake REST API भेजे गए token की परवाह किए बिना user name के रूप में "John Doe" return करती है।

:::

इस point पर हमने basic authentication flow set up कर लिया है। अगले चरण में हम सीखेंगे कि इसे अपने data provider के साथ कैसे integrate करें।

</Sandpack>
