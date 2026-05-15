# Refine Devtools Server

`@refinedev/devtools-server` は、開発中に Refine Devtools が使う server 層を含みます。production API を公開するためのものではなく、refine アプリケーションと Devtools UI をつなぐ役割を持ちます。

## パッケージの役割

Refine Devtools は、resources、providers、queries、mutations、実行時の状態を確認するための開発支援ツールです。このパッケージは `@refinedev/devtools` の一部として、通常は refine CLI か Devtools 連携から起動されます。

## インストール

多くのプロジェクトでは、公開 Devtools パッケージを追加すれば十分です。

```sh
npm install @refinedev/devtools
```

## ドキュメント

詳しい設定と使い方は、[Refine Devtools ドキュメント](https://refine.dev/docs/packages/devtools)を参照してください。
