# Integrasi Medusa Store

Package `@refinedev/medusa` menyediakan integrasi untuk store dan operational dashboard yang dibangun di atas Medusa. Package ini membantu menghubungkan lapisan data dan alur authentication dengan setup awal yang sederhana.

## Instalasi

```sh
npm install @refinedev/medusa
```

## Penggunaan dasar

```tsx
import dataProvider, { authProvider } from "@refinedev/medusa";

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider("API_URL")}
      authProvider={authProvider("API_URL")}
    >
      {/* ... */}
    </Refine>
  );
};
```

## Kapan digunakan?

Gunakan package ini saat Anda perlu membangun internal tools, dashboards, atau admin panel untuk backend commerce berbasis Medusa.

## Selengkapnya

Baca dokumentasi utama Refine dan materi Medusa untuk menyesuaikan authentication, resources, dan operasi katalog.
