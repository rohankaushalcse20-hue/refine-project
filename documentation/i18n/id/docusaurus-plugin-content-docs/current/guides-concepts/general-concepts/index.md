---
title: "Konsep Umum | Refine v5"
display_title: "Konsep Umum"
sidebar_label: "Konsep Umum"
description: "Pahami arsitektur headless Refine serta konsep resources, providers, hooks, dan meta."
---

Refine adalah framework yang dapat diperluas untuk membangun aplikasi web dengan cepat. Fondasinya adalah **hooks** dan **providers** yang dapat dikomposisi, dengan pola yang jelas untuk mengelola data dan state.

## Konsep headless

Refine tidak memaksa Anda memakai kumpulan komponen dengan tampilan tertentu. Refine menyediakan `hooks`, `components`, `providers`, dan helper, sementara lapisan UI tetap berada di bawah kendali Anda.

Karena itu, Anda dapat menggunakan Tailwind CSS, Ant Design, Material UI, Mantine, Chakra UI, atau design system sendiri bersama `@refinedev/core`.

## Konsep resource

**Resource** mewakili entitas aplikasi seperti `products`, `orders`, atau `blogPosts`. Definisi resource menghubungkan route, operasi CRUD, daftar, dan providers dalam satu struktur yang konsisten.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        show: "/products/:id",
        edit: "/products/:id/edit",
        create: "/products/new",
      },
    ]}
  />
);
```

## Providers

Providers adalah titik integrasi utama di Refine. Melalui providers, aplikasi mengelola data, authentication, authorization, notifications, i18n, routing, realtime, dan audit logs.

## Hooks

Hooks Refine bersifat headless dan tidak terikat pada library UI tertentu. Dengan `useGo`, `useCan`, `useTranslate`, dan hooks lainnya, Anda dapat menangani navigasi, izin, dan terjemahan melalui API yang seragam.

## Meta

Properti `meta` digunakan untuk mengirim informasi tambahan ke providers dan hooks, misalnya headers, parameter khusus, pemilihan field, atau konteks multi-tenant.
