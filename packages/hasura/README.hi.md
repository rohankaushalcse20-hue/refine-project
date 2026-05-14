# Hasura integration for refine

`@refinedev/hasura` Hasura-backed GraphQL APIs के लिए data provider देता है। यह Hasura endpoints, headers और Refine resources को जोड़कर admin panels और internal tools में CRUD operations चलाने में मदद करता है।

## Installation

```sh
npm install @refinedev/hasura
```

## Basic usage

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("HASURA_API_URL", {
  headers: {
    "x-hasura-role": "public",
  },
});

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

Hasura authorization rules और GraphQL schema के ऊपर Refine UI बनाते समय यह provider useful रहता है।

अधिक जानकारी के लिए [data provider documentation](https://refine.dev/docs/core/providers/data-provider) देखें।
