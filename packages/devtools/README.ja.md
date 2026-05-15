# refine Devtools

`@refinedev/devtools` は、開発中の refine アプリケーションを調査しやすくするためのツールです。queries と mutations の確認、Inferencer が生成したコードの試用、refine パッケージの管理などを UI から扱えます。

## 使い方

まず `@refinedev/cli` の最新バージョンをインストールします。

```bash
npm install @refinedev/cli@latest
```

CLI から `@refinedev/devtools` を追加します。

```bash
npm run refine devtools init
```

> `@refinedev/cli` をまだ追加していない場合は、プロジェクトに追加するための[インストールガイド](https://refine.dev/docs/packages/cli/#how-to-add-to-an-existing-project)を参照してください。

Devtools は開発モード向けの機能で、本番 build に余計な overhead を追加しません。

## ドキュメント

- [refine ドキュメント](https://refine.dev/docs/)を参照してください。
