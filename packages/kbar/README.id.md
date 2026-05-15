# Integrasi kbar untuk Refine

Package `@refinedev/kbar` menambahkan command palette berbasis [kbar](https://github.com/timc1/kbar) ke aplikasi Refine. Integrasi ini berguna untuk menyediakan navigasi cepat antarresources, actions, dan layar.

## Instalasi

```sh
npm install @refinedev/kbar
```

## Penggunaan dasar

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";

const App = () => (
  <RefineKbarProvider>
    <Refine>{/* ... */}</Refine>
    <RefineKbar />
  </RefineKbarProvider>
);
```

Integrasi ini menjaga actions Refine tetap sinkron dengan pengalaman pencarian dan navigasi di command palette.

## Dokumentasi

Baca [contoh command palette Refine](https://refine.dev/docs/examples/command-palette/) untuk opsi setup dan penggunaan.
