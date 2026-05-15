# GraphQL data provider

`@refinedev/graphql`, Refine projelerini ozel GraphQL backend'leriyle baglamak icin esnek bir data provider saglar. Kendi query, mutation ve transport kurallarini tanimlamak isteyen ekipler icin temel katman olarak kullanilir.

## Kurulum

```sh
npm install @refinedev/graphql
```

## Temel kullanim

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

## Ne zaman kullanilmali?

Backend'iniz GraphQL endpoint'i sunuyorsa ve Refine'in data katmanini kendi type'lariniza, resource'lariniza ve query aliskanliklariniza uyarlamak istiyorsaniz bu package'i kullanin.

## Dokumantasyon

Ayrintili entegrasyon icin [Refine GraphQL data provider dokumantasyonunu](https://refine.dev/docs/data/packages/graphql/) inceleyin.
