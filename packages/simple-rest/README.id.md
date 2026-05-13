# Simple REST data provider

`@refinedev/simple-rest` adalah data provider untuk REST APIs dengan struktur yang jelas. Package ini cocok saat Anda ingin menghubungkan `resources` di Refine langsung ke HTTP endpoints.

## Instalasi

```sh
npm install @refinedev/simple-rest
```

## Penggunaan dasar

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

Provider ini sesuai ketika backend menyediakan endpoints standar untuk operasi list, create, update, dan delete. Jika Anda membutuhkan headers atau params khusus, provider dapat dibungkus dan diperluas dengan mudah.
