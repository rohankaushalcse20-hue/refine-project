# NestJS Query data provider

`@refinedev/nestjs-query`, Refine uygulamalarini [NestJS Query](https://doug-martin.github.io/nestjs-query/) ile uretilen GraphQL API'lerine baglar. CRUD odakli NestJS backend'leri icin Refine data provider sozlesmesini hazirlar.

## Kurulum

```sh
npm install @refinedev/nestjs-query
```

## Temel kullanim

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/nestjs-query";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

Provider, NestJS Query semasindan gelen list, create, update ve delete islemlerini Refine resource'lariyla uyumlu hale getirir.

## Dokumantasyon

[Refine NestJS Query dokumantasyonunu](https://refine.dev/docs/data/packages/nestjs-query/) inceleyerek kurulum ve ozellestirme adimlarini takip edebilirsiniz.
