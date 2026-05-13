---
title: "Data Fetching | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "Pelajari hubungan antara data provider, resources, dan hooks data di Refine."
---

Data fetching di Refine berpusat pada `dataProvider`. Provider ini menerjemahkan operasi CRUD Refine menjadi panggilan ke API Anda, baik REST, GraphQL, maupun backend khusus.

## Data provider

`dataProvider` adalah objek dengan metode seperti `getList`, `getOne`, `create`, `update`, dan `deleteOne`. Hooks Refine memanggil metode ini berdasarkan resource dan action yang sedang dijalankan.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/simple-rest";

export const App = () => (
  <Refine dataProvider={dataProvider("https://api.fake-rest.refine.dev")} />
);
```

## Hooks data

Gunakan hooks seperti `useList`, `useOne`, `useCreate`, `useUpdate`, dan `useDelete` untuk membaca atau mengubah data. Hooks ini mengurus state loading, error, cache, invalidation, dan integrasi dengan resource.

## Resource dan endpoint

Nama resource biasanya dipakai untuk menentukan endpoint atau operasi backend. Misalnya resource `products` dapat dipetakan ke `/products`, sementara detail item memakai `id` yang dikirim oleh hook.

## Meta untuk kebutuhan khusus

Ketika endpoint membutuhkan informasi tambahan, gunakan `meta`. Nilai ini diteruskan ke data provider sehingga Anda dapat mengirim headers, query khusus, pemilihan fields, atau konteks lain tanpa mengubah API hook.

## Data tetap berada di bawah kendali Anda

Refine menyediakan pola fetching, mutasi, dan cache yang konsisten, tetapi bentuk response dan aturan backend tetap dapat disesuaikan di data provider.
