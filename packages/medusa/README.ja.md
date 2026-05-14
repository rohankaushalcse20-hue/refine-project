# Medusa store integration for refine

`@refinedev/medusa` は、Medusa backend を Refine の data provider と auth provider として利用するための package です。コマース管理、商品管理、注文管理などの画面を Refine で構築できます。

## インストール

```sh
npm install @refinedev/medusa
```

## 基本的な使い方

```tsx
import dataProvider, { authProvider } from "@refinedev/medusa";

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider("API_URL")}
      authProvider={authProvider("API_URL")}
    >
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

Medusa を backend にした EC 管理画面や社内運用ツールを、Refine の resource と認証フローに合わせて構築したい場合に使います。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine documentation](https://refine.dev/docs/)
- [refine tutorials](https://refine.dev/docs/tutorial/introduction/index/)
