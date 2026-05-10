---
title: "クイックスタート | Refine v5 のはじめ方"
display_title: "クイックスタートガイド"
sidebar_label: "クイックスタートガイド"
description: "ブラウザ版 scaffolder または CLI を使って Refine v5 プロジェクトを作成し、チュートリアルへ進みます。"
displayed_sidebar: mainSidebar
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import { Playground } from "@site/src/components/playground";

**Refine** は、Vite、Next.js、Remix、CRA など **React** を実行できる環境であれば動作します。

パッケージを手動で追加することもできますが、最もスムーズな始め方はブラウザ版 scaffolder か CLI を使うことです。どちらも、プロジェクト生成前に framework、UI、data provider、認証、i18n を選択できます。

## CLI を使う

`create-refine-app` を実行して、対話形式でプロジェクトを生成します。

```sh
npm create refine-app@latest
```

質問に答えたら生成されたディレクトリへ移動し、必要に応じて依存関係をインストールしてから、CLI が表示するコマンドで開発サーバーを起動してください。

## ブラウザを使う

ブラウザ版 scaffolder でも、CLI と同じ主要な選択肢を使えます。ダウンロード前に仕上がりを確認できる点も便利です。

<Playground />

## 次のステップ

[チュートリアル](/core/tutorial) に進んで初期プロジェクトを本格的な CRUD アプリケーションへ発展させるか、[実例テンプレート](/core/templates) を確認し、[基本概念](/core/docs/guides-concepts/general-concepts/) や [data fetching](/core/docs/guides-concepts/data-fetching/) のガイドもあわせて参照してください。
