---
title: "Tables | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "Refine'ın resource'a bağlı list ve table sayfaları oluşturmaya nasıl yardımcı olduğunu öğrenin."
---

Table sayfaları çoğu CRUD iş akışının merkezidir. Refine, liste verisini almak, pagination, sorting, filtering yönetmek ve table aksiyonlarını resource ile bağlamak için hooks sağlar.

## List hooks

Liste verisi almak için `useTable` veya seçtiğiniz UI framework'ün table entegrasyonunu kullanın. Hook, aktif resource üzerinden data provider ile konuşur.

```tsx title=PostList.tsx
import { useTable } from "@refinedev/core";

export const PostList = () => {
  const { tableQuery } = useTable({ resource: "posts" });

  return <pre>{JSON.stringify(tableQuery.data, null, 2)}</pre>;
};
```

## Pagination, sorting ve filtering

Refine table state'ini data provider'a aktarır; böylece backend pagination, sorter ve filter parametrelerini alabilir. Bu kalıp, küçük ve büyük tabloların aynı API ile çalışmasını sağlar.

## Record actions

Edit, show ve delete gibi butonlar resource metadata üzerinden oluşturulabilir. Böylece URL'ler ve izinler uygulama yapılandırmasıyla tutarlı kalır.

## UI entegrasyonu

Refine hem headless yaklaşımı hem de birkaç UI framework için hazır entegrasyonları destekler. Ana data contract değişmeden en uygun table component'ini seçebilirsiniz.
