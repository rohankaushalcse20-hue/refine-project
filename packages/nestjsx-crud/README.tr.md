# Nestjsx CRUD data provider

`@refinedev/nestjsx-crud`, Refine'i [@nestjsx/crud](https://github.com/nestjsx/crud) ile olusturulan REST API'lerle kullanmak icin data provider saglar. NestJS tabanli CRUD endpoint'lerini Refine resource operasyonlarina baglar.

## Kurulum

```sh
npm install @refinedev/nestjsx-crud
```

## Temel kullanim

```tsx
import dataProvider from "@refinedev/nestjsx-crud";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

## Ne zaman kullanilmali?

Backend'iniz NestJS ve `@nestjsx/crud` ile standart REST endpoint'leri uretiyorsa, Refine tarafinda listeleme, filtreleme, siralama ve CRUD aksiyonlarini hizlica baglamak icin kullanin.

## Dokumantasyon

Kurulum ve API uyarlama ayrintilari icin [Refine Nestjsx CRUD dokumantasyonunu](https://refine.dev/docs/data/packages/nestjsx-crud/) inceleyin.
