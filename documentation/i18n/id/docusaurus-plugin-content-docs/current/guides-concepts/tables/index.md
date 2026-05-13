---
title: "Tables | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "Pelajari bagaimana Refine membantu membuat halaman list dan table yang terhubung ke resource."
---

Halaman table biasanya menjadi pusat workflow CRUD. Refine menyediakan hooks untuk mengambil daftar data, mengelola pagination, sorting, filtering, dan menghubungkan aksi table ke resource.

## List hooks

Gunakan `useTable` atau integrasi table dari UI framework pilihan Anda untuk mengambil data list. Hook ini berbicara dengan data provider melalui resource yang sedang aktif.

```tsx title=PostList.tsx
import { useTable } from "@refinedev/core";

export const PostList = () => {
  const { tableQuery } = useTable({ resource: "posts" });

  return <pre>{JSON.stringify(tableQuery.data, null, 2)}</pre>;
};
```

## Pagination, sorting, dan filtering

Refine meneruskan state table ke data provider, sehingga backend dapat menerima parameter pagination, sorter, dan filter. Dengan pola ini, table kecil maupun besar tetap memakai API yang sama.

## Aksi record

Tombol seperti edit, show, dan delete dapat dibangun dari metadata resource. Ini membuat URL dan izin tetap konsisten dengan konfigurasi aplikasi.

## Integrasi UI

Refine mendukung pendekatan headless dan integrasi siap pakai untuk beberapa UI framework. Anda dapat memilih komponen table yang paling cocok tanpa mengubah kontrak data utama.
