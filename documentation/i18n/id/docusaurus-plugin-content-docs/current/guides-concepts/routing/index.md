---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Pelajari bagaimana Refine menghubungkan resources, route actions, dan router provider."
---

Refine tidak membawa router sendiri. Sebaliknya, Refine berbicara dengan router melalui `routerProvider`, sehingga aplikasi dapat memakai React Router, Next.js, Remix, atau integrasi routing lain.

## Router provider

`routerProvider` memberi Refine cara untuk membaca lokasi saat ini, membuat link, dan menjalankan navigasi. Integrasi resmi seperti `@refinedev/react-router` sudah menyediakan implementasi yang sesuai.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";

export const App = () => (
  <Refine
    routerProvider={routerProvider}
    resources={[
      {
        name: "posts",
        list: "/posts",
        create: "/posts/create",
        edit: "/posts/edit/:id",
        show: "/posts/show/:id",
      },
    ]}
  />
);
```

## Route actions

Setiap resource dapat memiliki route untuk action seperti `list`, `create`, `edit`, dan `show`. Refine memakai metadata ini untuk membangun navigasi, breadcrumbs, tombol aksi, dan redirect yang konsisten.

## Navigasi terprogram

Gunakan hooks seperti `useGo`, `useBack`, dan `useGetToPath` ketika Anda perlu berpindah halaman dari kode aplikasi. Hooks ini menjaga navigasi tetap selaras dengan resource dan router yang sedang digunakan.

## Menjaga URL tetap eksplisit

Refine bekerja paling baik ketika URL resource ditulis eksplisit. Pola ini membuat menu, permissions, dan deep links lebih mudah dipahami oleh tim serta lebih aman saat aplikasi bertambah besar.
