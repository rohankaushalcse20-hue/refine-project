# NestJS Query data provider integration for refine

`@refinedev/nestjs-query` NestJS Query GraphQL APIs के लिए data provider और live provider देता है। यह GraphQL client और subscription transport को Refine के CRUD और realtime workflows से जोड़ता है।

## Installation

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## Basic usage

```tsx
import dataProvider, {
  GraphQLClient,
  liveProvider,
} from "@refinedev/nestjs-query";

import { createClient } from "graphql-ws";

const App = () => (
  <Refine
    dataProvider={dataProvider(new GraphQLClient("API_URL"))}
    liveProvider={liveProvider(createClient({ url: "WS_URL" }))}
  >
    {/* ... */}
  </Refine>
);
```

NestJS Query schema और GraphQL subscriptions के साथ Refine app बनाते समय यह integration useful है।

अधिक जानकारी के लिए [data provider documentation](https://refine.dev/docs/core/providers/data-provider) और [NestJS Query example](https://refine.dev/docs/examples/data-provider/nestjs-query/) देखें।
