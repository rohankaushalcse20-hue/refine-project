# NestJSX CRUD data provider integration for refine

`@refinedev/nestjsx-crud` NestJSX CRUD style REST APIs के लिए data provider देता है। यह NestJS-based endpoints को Refine resources और CRUD hooks से जोड़ता है।

## Installation

```sh
npm install @refinedev/nestjsx-crud
```

## Basic usage

```tsx
import dataProvider from "@refinedev/nestjsx-crud";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

अगर आपकी API NestJSX CRUD conventions follow करती है, तो यह package mapping और request handling को सरल बनाता है।

अधिक जानकारी के लिए [data provider documentation](https://refine.dev/docs/core/providers/data-provider) और [NestJS CRUD example](https://refine.dev/docs/examples/data-provider/nestjsxCrud/) देखें।
