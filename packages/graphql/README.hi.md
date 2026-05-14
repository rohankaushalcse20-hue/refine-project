# GraphQL integration for refine

`@refinedev/graphql` GraphQL APIs के लिए data provider देता है। यह Refine resources को GraphQL queries और mutations से जोड़ता है, ताकि list, create, update और delete workflows framework के standard data provider contract से चल सकें।

## Installation

```sh
npm install @refinedev/graphql
```

## Basic usage

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

जब आपका backend GraphQL schema expose करता हो और आप Refine hooks के साथ same CRUD flow रखना चाहते हों, तब यह package अच्छा विकल्प है।

Documentation के लिए [data provider guide](https://refine.dev/docs/core/providers/data-provider) और [GraphQL package docs](https://refine.dev/docs/packages/documentation/data-providers/graphql/) देखें।
