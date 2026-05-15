# Refine icin Ably entegrasyonu

`@refinedev/ably`, Refine uygulamalarina [Ably](https://ably.com/) tabanli bir `liveProvider` ekler. Internal tool, dashboard veya admin panelinizin realtime guncellemelere ihtiyaci varsa bu package uygun bir baslangic noktasi saglar.

## Kurulum

```sh
npm install @refinedev/ably
```

## Temel kullanim

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => (
  <Refine liveProvider={liveProvider(ablyClient)}>
    {/* ... */}
  </Refine>
);
```

Provider, Ably olaylarini Refine'in realtime sozlesmesine baglar ve veri mantigini UI katmanindan ayri tutar.

## Dokumantasyon

- [Refine live provider dokumantasyonunu](https://refine.dev/docs/api-references/providers/live-provider/) inceleyin.
- [Ably ile Refine tutorial'ini](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine) da takip edebilirsiniz.
