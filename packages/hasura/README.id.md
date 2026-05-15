# Integrasi Hasura

Package `@refinedev/hasura` menghubungkan Refine dengan project Hasura dan menyederhanakan penggunaan GraphQL pada aplikasi CRUD. Ini cocok saat Anda bekerja dengan queries, mutations, dan subscriptions dari backend yang mengikuti ekosistem Hasura.

## Instalasi

```sh
npm install @refinedev/hasura
```

## Penggunaan dasar

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("HASURA_API_URL", {
  headers: {
    "x-hasura-role": "public",
  },
});

const App = () => {
  return (
    <Refine dataProvider={dataProvider(client)}>
      {/* ... */}
    </Refine>
  );
};
```

## Kapan digunakan?

Gunakan package ini saat project Anda memakai Hasura untuk menyediakan GraphQL, mengelola roles, atau menambahkan kemampuan realtime melalui integrasi siap pakai.

## Selengkapnya

Baca dokumentasi data providers Refine dan panduan Hasura untuk menyesuaikan integrasi dengan schema project Anda.
