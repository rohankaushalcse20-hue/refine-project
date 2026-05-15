# Hasura data provider

`@refinedev/hasura`, Refine uygulamalarini [Hasura](https://hasura.io/) GraphQL API'leriyle entegre eder. Hasura uzerindeki tablolar ve iliskiler icin CRUD ekranlari kurarken Refine resource modelini kullanmanizi saglar.

## Kurulum

```sh
npm install @refinedev/hasura
```

## Temel kullanim

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("YOUR_HASURA_GRAPHQL_ENDPOINT", {
  headers: {
    "x-hasura-role": "admin",
  },
});

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

Provider, Hasura GraphQL semasini Refine'in list, create, update ve delete operasyonlariyla kullanmaya yardim eder.

## Dokumantasyon

[Refine Hasura data provider dokumantasyonunda](https://refine.dev/docs/data/packages/hasura/) kurulum ve kullanim ayrintilarini bulabilirsiniz.
