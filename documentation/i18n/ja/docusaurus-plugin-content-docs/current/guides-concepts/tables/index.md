---
title: "テーブルと一覧 | Refine v5"
display_title: "テーブル"
sidebar_label: "テーブル"
description: "Refine を使って tables、lists、filters、sorting、pagination を構築します。"
---

テーブルと一覧は、API のデータを探索しやすい UI に変換します。Refine には、pagination、filters、sorting、loading state を data provider と接続する hooks があります。

## 一覧表示

`useTable` と `useList` は一覧画面の土台です。UI integration と一緒にも、独自 components と一緒にも使えます。

```tsx
const table = useTable({
  resource: "products",
  pagination: { pageSize: 10 },
});
```

## フィルタと並び替え

filters と sorters は、data provider が API に渡せるパラメータへ変換されます。これにより UI と backend 通信の結合を弱められます。

## CRUD actions

一覧に create、edit、show、delete の buttons を組み合わせましょう。actions は access control provider の権限を尊重し、labels を i18n で翻訳できます。

## ユーザー体験

読み込み中、空状態、エラー状態を明確に表示してください。大きなテーブルでは pagination や段階読み込みを使い、UI の応答性を保つのが有効です。
