# Remix router provider for refine

`@refinedev/remix-router` は、Remix の routing を Refine の router provider として使うための package です。Remix アプリケーションで resource ベースの navigation と Refine の routing hooks を連携できます。

## インストール

```sh
npm install @refinedev/remix-router
```

## できること

- Refine の route 生成と navigation を Remix に接続する。
- `resources` に定義した CRUD 画面へ一貫した方法で遷移する。
- 認証や redirect の流れを Remix の routing と組み合わせる。

## 使いどころ

Remix を使った Refine アプリケーションで、resource 定義を中心にした画面遷移と URL 管理を行いたい場合に使います。

## 詳細

詳細な利用方法は [refine router provider documentation](https://refine.dev/docs/core/providers/router-provider/) を参照してください。
