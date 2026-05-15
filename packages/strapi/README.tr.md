# Refine için Strapi entegrasyonu

`@refinedev/strapi`, Refine uygulamalarını [Strapi](https://strapi.io/) backend'leriyle bağlayan data provider package'ıdır. Strapi kaynakları üzerinde admin panel ve CRUD ekranları oluştururken Refine'ın resource workflow'larını kullanmanızı sağlar.

## Kurulum

```sh
npm install @refinedev/strapi
```

## Temel kullanım

```tsx
import dataProvider from "@refinedev/strapi";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

## Dokümantasyon

- [Refine data provider dokümantasyonunu](https://refine.dev/docs/core/providers/data-provider) okuyun.
- [Strapi data provider dokümantasyonunu](https://refine.dev/docs/packages/documentation/data-providers/strapi/) inceleyin.
