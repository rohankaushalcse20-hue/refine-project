# NestJS Query data provider untuk Refine

Package `@refinedev/nestjs-query` menghubungkan Refine dengan APIs yang dibangun menggunakan [NestJS Query](https://doug-martin.github.io/nestjs-query/). Package ini menyertakan data provider dan live provider untuk bekerja dengan GraphQL dan subscriptions.

## Instalasi

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## Penggunaan dasar

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

## Dokumentasi

Baca [dokumentasi data providers Refine](https://refine.dev/docs/data/data-provider/) dan referensi NestJS Query untuk menyesuaikan resources, filters, dan relasi.
