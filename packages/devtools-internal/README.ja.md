# Refine Devtools 内部パッケージ

`@refinedev/devtools-internal` は、Refine Devtools の各パッケージで共有される内部ユーティリティを含みます。`@refinedev/devtools` の実装を支えるパッケージであり、アプリケーション向けの公開 API として使うものではありません。

## パッケージの役割

Refine Devtools は、開発中のアプリケーションで resources、providers、queries、mutations、イベントを確認するための機能です。このパッケージは、その体験を一貫させるために Devtools パッケージ群で使う内部部品をまとめています。

## インストール

通常、このパッケージを直接インストールする必要はありません。公開パッケージから Devtools を導入してください。

```sh
npm install @refinedev/devtools
```

## ドキュメント

推奨される設定と利用の流れは、[Refine Devtools ドキュメント](https://refine.dev/docs/packages/devtools)を参照してください。
