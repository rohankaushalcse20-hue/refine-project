# Integrasi Appwrite untuk Refine

Package `@refinedev/appwrite` menghubungkan aplikasi Refine dengan project [Appwrite](https://appwrite.io/). Package ini menyertakan helper untuk `dataProvider`, `liveProvider`, dan authentication sehingga aplikasi CRUD dapat memakai Appwrite APIs tanpa terikat ke UI tertentu.

## Instalasi

```sh
npm install @refinedev/appwrite
```

## Penggunaan dasar

```tsx
import { dataProvider, liveProvider } from "@refinedev/appwrite";

const App = () => (
  <Refine
    dataProvider={dataProvider(appwriteClient, {
      databaseId: "DATABASE_ID",
    })}
    liveProvider={liveProvider(appwriteClient, {
      databaseId: "DATABASE_ID",
    })}
  >
    {/* ... */}
  </Refine>
);
```

## Dokumentasi

Baca [dokumentasi Refine](https://refine.dev/docs/) untuk detail tentang data providers, realtime, dan authentication.
