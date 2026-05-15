# Integrasi Ably untuk Refine

Package `@refinedev/ably` menyediakan `liveProvider` berbasis [Ably](https://ably.com/) untuk aplikasi Refine. Gunakan saat internal tool, dashboard, atau admin panel membutuhkan pembaruan realtime melalui koneksi WebSocket.

## Instalasi

```sh
npm install @refinedev/ably
```

## Penggunaan dasar

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => (
  <Refine liveProvider={liveProvider(ablyClient)}>
    {/* ... */}
  </Refine>
);
```

Provider ini menghubungkan event Ably ke kontrak realtime Refine sambil menjaga logika data tetap terpisah dari lapisan UI.

## Dokumentasi

- Baca [dokumentasi live provider Refine](https://refine.dev/docs/api-references/providers/live-provider/).
- Baca juga [tutorial resmi Ably dengan Refine](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine).
