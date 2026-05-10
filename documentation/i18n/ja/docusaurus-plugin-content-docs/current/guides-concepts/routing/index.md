---
title: "ルーティング | Refine v5"
display_title: "ルーティング"
sidebar_label: "ルーティング"
description: "React Router、Next.js、Remix などを使って Refine の routing を構成する方法を紹介します。"
---

routing は CRUD アプリケーションの中心です。Refine の headless アーキテクチャにより、特定の framework に縛られずに好きなルーターを選べます。

Refine には **React Router**、**Next.js**、**Remix** 向けの統合が用意されており、次のような利点があります。

- hooks や components でパラメータを自動検出できる
- mutation や認証状態の変化後にリダイレクトできる
- ナビゲーション、breadcrumbs、メニュー用のユーティリティを使える

Refine は router 非依存なので、アプリケーションのルート定義自体は引き続き自分で管理します。React Router では `Routes`、Next.js では `pages` または `app`、Remix では `app/routes` を使います。

## Router provider を統合する

使いたい統合を import し、`<Refine />` の `routerProvider` に渡します。

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Routes } from "react-router";

export const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* あなたのルート */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

## ベストプラクティス

routes と resources の対応を揃え、命名を統一し、可能な限り `resource` や `id` などのパラメータは router から hooks に受け渡すようにしましょう。
