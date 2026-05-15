# Integrasi Airtable untuk Refine

Package `@refinedev/airtable` menyediakan data provider untuk menghubungkan aplikasi Refine dengan base [Airtable](https://www.airtable.com/). Integrasi ini cocok untuk membangun admin panel dan alat CRUD di atas data yang sudah tersimpan di Airtable.

## Instalasi

```sh
npm install @refinedev/airtable
```

## Penggunaan dasar

```tsx
import dataProvider from "@refinedev/airtable";

const App = () => (
  <Refine dataProvider={dataProvider("API_KEY", "BASE_ID")}>
    {/* ... */}
  </Refine>
);
```

Provider ini menerjemahkan operasi `resource` di Refine menjadi panggilan ke Airtable API tanpa memaksakan library UI tertentu.

## Dokumentasi

- Baca [dokumentasi data providers Refine](https://refine.dev/docs/data/data-provider/).
- Baca [dokumentasi utama Refine](https://refine.dev/docs/) untuk guides dan tutorials.
