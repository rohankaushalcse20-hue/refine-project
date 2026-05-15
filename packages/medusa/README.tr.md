# Medusa data provider

`@refinedev/medusa`, Refine uygulamalarini [Medusa](https://medusajs.com/) backend'leriyle calistirmak icin data provider saglar. E-commerce operasyon ekranlari, katalog yonetimi ve admin deneyimleri olustururken Refine kaynaklarini Medusa API'lerine baglar.

## Kurulum

```sh
npm install @refinedev/medusa
```

## Temel kullanim

```tsx
import dataProvider from "@refinedev/medusa";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

## Ne zaman kullanilmali?

Medusa uzerinde calisan commerce verileri icin listeleme, olusturma, guncelleme ve silme ekranlarini Refine ile hizli kurmak istediginizde kullanin.

## Dokumantasyon

Paket ayrintilari ve data provider davranisi icin [Refine dokumantasyonunu](https://refine.dev/docs/) inceleyin.
