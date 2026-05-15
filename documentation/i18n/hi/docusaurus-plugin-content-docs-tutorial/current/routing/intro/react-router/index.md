---
title: परिचय
---

import { Sandpack, AddRouterProviderToApp } from "./sandpack.tsx";

<Sandpack>

अब हमने Refine में data fetching essentials और authentication की basics सीख ली हैं। इस unit में हम सीखेंगे कि अपनी app में router provider कैसे जोड़ें और router provider से कौन-कौन सी features unlock होती हैं।

Refine सबसे लोकप्रिय routing options के लिए integrations देता है, जैसे [React Router](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js), और [Remix](/core/docs/routing/integrations/remix)।

:::simple Implementation Tips

- अपने router के लिए built-in integration चुनना recommended है, लेकिन अगर आप custom solution चाहते हैं, तो Refine के आसान [router provider interface](/core/docs/routing/router-provider) से अपना provider बना सकते हैं।

- Refine आपके router के navigation handle करने के तरीके में interfere नहीं करेगा। आप routes/pages वैसे ही generate करेंगे जैसे सामान्य रूप से अपने router के साथ करते हैं।

- Refine को router provider देने से आपके router की existing features छोड़े बिना कई Refine features unlock होती हैं।

:::

यह unit इन topics को cover करेगी:

- Refine का resource concept और उसका उपयोग,
- URL से `resource`, `action`, और `id` जैसे parameters infer करने के लिए router integration का उपयोग,
- Refine में navigation और redirections handle करना,
- Form और table states को URL में store करने के लिए router integration का उपयोग,
- अंत में, router options के साथ authentication handle करना।

यह unit UI framework agnostic रहेगी। UI frameworks के लिए routing से जुड़े related parts अगले units में cover होंगे।

## Router Provider जोड़ना

Dependencies जोड़कर शुरू करते हैं। Routing के लिए हम `react-router` का उपयोग करेंगे, और इसे Refine के साथ integrate करने के लिए `@refinedev/react-router` package का उपयोग करेंगे।

<InstallPackagesCommand args="react-router @refinedev/react-router"/>

फिर हम अपना router provider `<Refine />` component को pass करेंगे। इसके साथ, हम अपनी app को `react-router` के `<BrowserRouter />` से wrap करेंगे।

अपने `src/App.tsx` file में ये lines जोड़कर update करें:

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";
// highlight-next-line
import routerProvider from "@refinedev/react-router";

// highlight-next-line
import { BrowserRouter } from "react-router";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

import { Login } from "./pages/login";
import { Header } from "./components/header";

export default function App(): JSX.Element {
  return (
    // highlight-next-line
    <BrowserRouter>
      <Refine
        dataProvider={dataProvider}
        authProvider={authProvider}
        // highlight-next-line
        routerProvider={routerProvider}
      >
        <Authenticated key="protected" fallback={<Login />}>
          <Header />
          {/* <ShowProduct /> */}
          {/* <EditProduct /> */}
          <ListProducts />
          {/* <CreateProduct /> */}
        </Authenticated>
      </Refine>
      {/* highlight-next-line */}
    </BrowserRouter>
  );
}
```

<AddRouterProviderToApp />

अब हम Refine के router integration की features explore करने के लिए तैयार हैं।

अगले step में हम सीखेंगे कि हर resource से related routes के बारे में Refine को कैसे बताएं।

</Sandpack>
