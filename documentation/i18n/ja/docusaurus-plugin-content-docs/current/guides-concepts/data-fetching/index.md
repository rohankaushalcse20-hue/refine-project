---
title: "データ取得 | Refine v5"
display_title: "データ取得"
sidebar_label: "データ取得"
description: "data providers と hooks を使って、Refine が UI と API をどのようにつなぐかを学びます。"
---

管理画面ではデータが中心です。Refine は [`DataProvider`](/core/docs/core/interface-references#dataprovider) インターフェースを実装した `dataProvider` を通じて、UI を 1 つ以上のデータソースに接続します。

data provider は `resource`、`id`、`meta` などの情報を受け取り、API の正しい endpoint を呼び出します。

## データ用 hooks

data provider を登録すると、`useList`、`useOne`、`useCreate`、`useUpdate`、`useDelete` のような hooks で CRUD 操作を扱えます。

```tsx
import { useOne } from "@refinedev/core";

const Product = () => {
  const { data, isLoading } = useOne({
    resource: "products",
    id: 1,
  });

  if (isLoading) return <span>Loading...</span>;
  return <pre>{JSON.stringify(data, null, 2)}</pre>;
};
```

## 状態とキャッシュ

データ hooks の内部では TanStack Query が使われています。これにより、読み込み・エラー・成功状態、キャッシュ、request の重複排除、自動 invalidation、optimistic update を利用できます。

## 複数 providers

resource ごとに異なる provider を使うこともできます。たとえば `posts` は REST、`users` は GraphQL という構成でも、components 側の API は一貫したままです。
