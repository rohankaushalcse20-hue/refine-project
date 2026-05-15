# GraphQL data provider

Package `@refinedev/graphql` menyediakan data provider untuk menghubungkan project Refine dengan backend GraphQL kustom. Ini menjadi dasar yang fleksibel saat Anda perlu menentukan queries, mutations, dan aturan transport sendiri.

## Instalasi

```sh
npm install @refinedev/graphql
```

## Penggunaan dasar

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => {
  return (
    <Refine dataProvider={dataProvider(client)}>
      {/* ... */}
    </Refine>
  );
};
```

## Kapan digunakan?

Gunakan package ini saat backend menyediakan endpoint GraphQL dan Anda perlu menyesuaikan lapisan data Refine dengan types, resources, dan aturan query project.

## Selengkapnya

Baca dokumentasi GraphQL data provider Refine untuk memperluas integrasi.
