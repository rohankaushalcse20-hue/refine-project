# Refine Devtools 共有ユーティリティ

`@refinedev/devtools-shared` は、Refine Devtools のパッケージ間で共有される型、定数、ユーティリティを含みます。アプリケーション、server、Devtools UI 間の通信をそろえるための内部基盤です。

## いつ使うか

このパッケージは主に Devtools の内部実装向けです。一般的な refine アプリケーションでは、公開パッケージをインストールして設定します。

```sh
npm install @refinedev/devtools
```

## 注意点

- イベント名、payload、内部 contracts はコードと同じ名前のまま扱います。
- このパッケージは `@refinedev/devtools` のバージョンに追従します。
- Devtools の公開 API はメインのドキュメントで確認してください。

## ドキュメント

インストールと利用の詳細は、[Refine Devtools ドキュメント](https://refine.dev/docs/packages/devtools)を参照してください。
