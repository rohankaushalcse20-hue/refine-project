# Refine icin Appwrite entegrasyonu

`@refinedev/appwrite`, Refine uygulamalarini [Appwrite](https://appwrite.io/) projeleriyle baglar. `dataProvider`, `liveProvider` ve authentication akislari icin yardimcilar sunarak CRUD uygulamalarinin Appwrite API'lerini UI katmanina bagimli olmadan kullanmasini saglar.

## Kurulum

```sh
npm install @refinedev/appwrite
```

## Temel kullanim

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

Bu paket, Appwrite veritabanlarini ve realtime ozelliklerini Refine resource modeliyle birlikte kullanmak isteyen ekipler icin uygundur.

## Dokumantasyon

[Refine Appwrite dokumantasyonunda](https://refine.dev/docs/data/packages/appwrite/) data provider kurulumu ve ilgili API ayrintilarini bulabilirsiniz.
