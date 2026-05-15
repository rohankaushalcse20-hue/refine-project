# Refine için Strapi v4 entegrasyonu

`@refinedev/strapi-v4`, Strapi v4 API'leriyle çalışan Refine uygulamaları için data provider sağlar. Strapi v4 collection types üzerinde CRUD ekranları, admin panel ve internal tool geliştirmek için kullanılır.

## Kurulum

```sh
npm install @refinedev/strapi-v4
```

## Temel kullanım

```tsx
import { DataProvider } from "@refinedev/strapi-v4";

const App = () => (
  <Refine dataProvider={DataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

## Dokümantasyon

- [Refine data provider dokümantasyonunu](https://refine.dev/docs/core/providers/data-provider) okuyun.
- [Strapi v4 data provider dokümantasyonunu](https://refine.dev/docs/packages/documentation/data-providers/strapi-v4/) inceleyin.
- [Strapi v4 örneğini](https://refine.dev/docs/examples/data-provider/strapi-v4/) açın.
