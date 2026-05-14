# React Router provider for refine

`@refinedev/react-router` は、React Router を Refine の router provider として使うための package です。resource に基づくページ遷移、URL 生成、認証後の redirect などを React Router の構成に接続します。

## インストール

```sh
npm install @refinedev/react-router
```

## できること

- Refine の routing hooks を React Router 上で動かす。
- `resources` で定義した list、show、create、edit 画面へ移動する。
- 認証や access control と組み合わせて route を保護する。

## 使いどころ

Vite や SPA 構成の React アプリケーションで、Refine の routing 機能を React Router に合わせて使いたい場合に適しています。

## 詳細

詳細な利用方法は [refine router provider documentation](https://refine.dev/docs/core/providers/router-provider/) を参照してください。
