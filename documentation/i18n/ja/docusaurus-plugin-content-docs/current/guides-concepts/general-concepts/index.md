---
title: "基本概念 | Refine v5"
display_title: "基本概念"
sidebar_label: "基本概念"
description: "Refine の基礎となる headless アーキテクチャ、resources、providers、hooks、meta を学びます。"
---

Refine は、Web アプリケーションをすばやく構築するための拡張性の高いフレームワークです。**hooks**、差し替え可能な **providers**、そして堅牢なデータ・状態管理を土台にしています。

## Headless の考え方

Refine は、特定の見た目のコンポーネントセットを強制しません。代わりに `hooks`、`components`、`providers`、ユーティリティを提供し、ビジネスロジックと UI を分離します。

そのため、独自のデザインシステムや Tailwind CSS、Ant Design、Material UI、Mantine、Chakra UI を使いながら、`@refinedev/core` の利点を活かせます。

## Resource

**resource** は、`products`、`blogPosts`、`orders` のようなアプリケーション内のエンティティを表します。resource 定義によって、ルート、CRUD 操作、メニュー、providers が一つの構造にまとまります。

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

providers は、データ、認証、認可、通知、i18n、リアルタイム、routing、監査といった重要な領域を担当します。組み込み providers を使うことも、独自実装を用意することもできます。

## Hooks

Refine の hooks は headless でライブラリ非依存です。`useGo`、`useCan`、`useTranslate` のような API により、ナビゲーション、権限、翻訳を一貫した形で扱えます。

## Meta

`meta` プロパティを使うと、providers や hooks に追加情報を渡せます。header、特殊なパラメータ、フィールド選択、multi-tenancy、GraphQL クエリの指定などに役立ちます。
