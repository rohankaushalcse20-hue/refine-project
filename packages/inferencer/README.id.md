# Refine Inferencer

Package `@refinedev/inferencer` menghasilkan UI CRUD dari struktur data Anda agar Anda bisa mulai cepat lalu menyesuaikan hasilnya secara manual. Package ini berguna saat mengeksplorasi API atau membuat versi awal admin panel.

## Instalasi

```sh
npm install @refinedev/inferencer
```

## Penggunaan dasar

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";

const App = () => {
  return (
    <Refine>
      <AntdInferencer action="list" resource="posts" />
    </Refine>
  );
};
```

## Kapan digunakan?

Gunakan Inferencer saat Anda membutuhkan prototyping cepat untuk layar CRUD, memeriksa bentuk API, atau membuat rancangan awal yang bisa diedit.

## Selengkapnya

Baca dokumentasi Inferencer dan tutorial Refine untuk menyesuaikan UI yang dihasilkan dengan project Anda.
