# Medusa store integration for refine

`@refinedev/medusa` Medusa commerce backends के लिए data provider और auth helper देता है। इससे Refine applications में products, orders और commerce workflows को Medusa API से जोड़ा जा सकता है।

## Installation

```sh
npm install @refinedev/medusa
```

## Basic usage

```tsx
import dataProvider, { authProvider } from "@refinedev/medusa";

const App = () => (
  <Refine
    dataProvider={dataProvider("API_URL")}
    authProvider={authProvider("API_URL")}
  >
    {/* ... */}
  </Refine>
);
```

Medusa store operations के ऊपर admin या internal commerce tooling बनाते समय यह package उपयोगी है।

अधिक जानकारी के लिए [data provider documentation](https://refine.dev/docs/core/providers/data-provider) देखें।
