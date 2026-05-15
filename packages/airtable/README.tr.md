# Refine icin Airtable entegrasyonu

`@refinedev/airtable`, Refine uygulamalarini [Airtable](https://www.airtable.com/) base'leriyle calistirmak icin bir data provider saglar. Airtable'da tutulan veriler uzerine CRUD panelleri, operasyon ekranlari veya kucuk internal tools kurarken kullanislidir.

## Kurulum

```sh
npm install @refinedev/airtable
```

## Temel kullanim

```tsx
import dataProvider from "@refinedev/airtable";

const App = () => (
  <Refine dataProvider={dataProvider("API_KEY", "BASE_ID")}>
    {/* ... */}
  </Refine>
);
```

Provider, Refine resource operasyonlarini Airtable API cagrisina cevirir ve belirli bir UI library zorunlu kilmaz.

## Dokumantasyon

- [Refine data provider dokumantasyonunu](https://refine.dev/docs/data/data-provider/) inceleyin.
- Daha fazla rehber ve tutorial icin [Refine dokumantasyonuna](https://refine.dev/docs/) bakin.
