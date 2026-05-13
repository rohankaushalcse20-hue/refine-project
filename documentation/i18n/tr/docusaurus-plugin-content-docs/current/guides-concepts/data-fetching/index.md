---
title: "Data Fetching | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "Refine'da data provider, resources ve data hooks arasındaki ilişkiyi öğrenin."
---

Refine'da data fetching `dataProvider` etrafında şekillenir. Bu provider, Refine CRUD işlemlerini REST, GraphQL veya özel backend çağrılarınıza çevirir.

## Data provider

`dataProvider`, `getList`, `getOne`, `create`, `update` ve `deleteOne` gibi metotlara sahip bir nesnedir. Refine hooks, çalışan resource ve action'a göre bu metotları çağırır.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/simple-rest";

export const App = () => (
  <Refine dataProvider={dataProvider("https://api.fake-rest.refine.dev")} />
);
```

## Data hooks

Veri okumak veya değiştirmek için `useList`, `useOne`, `useCreate`, `useUpdate` ve `useDelete` gibi hooks kullanın. Bu hooks loading state, error state, cache, invalidation ve resource entegrasyonunu yönetir.

## Resource ve endpoint

Resource adı çoğunlukla endpoint veya backend operasyonunu belirlemek için kullanılır. Örneğin `products` resource'u `/products` endpoint'ine bağlanabilir; kayıt detayı hook tarafından gönderilen `id` ile alınır.

## Özel ihtiyaçlar için meta

Endpoint ek bilgi gerektirdiğinde `meta` kullanın. Bu değer data provider'a aktarılır; böylece hook API'sini değiştirmeden headers, özel query değerleri, field seçimleri veya başka bağlamlar gönderebilirsiniz.

## Veri sizin kontrolünüzde kalır

Refine fetching, mutation ve cache için tutarlı bir kalıp sağlar; ancak response şekli ve backend kuralları data provider içinde özelleştirilebilir.
