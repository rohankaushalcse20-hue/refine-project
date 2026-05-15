# NestJS Query data provider لـ Refine

تربط حزمة `@refinedev/nestjs-query` بين Refine وAPIs المبنية على [NestJS Query](https://doug-martin.github.io/nestjs-query/). وهي تتضمن data provider وlive provider للعمل مع GraphQL وsubscriptions.

## التثبيت

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## الاستخدام الأساسي

```tsx
import dataProvider, { GraphQLClient, liveProvider } from "@refinedev/nestjs-query";
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

## التوثيق

راجع [توثيق data providers في Refine](https://refine.dev/docs/data/data-provider/) ومرجع NestJS Query لتكييف resources وfilters والعلاقات.
