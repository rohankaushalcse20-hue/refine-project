# Hasura integration for refine

`@refinedev/hasura` は、Hasura が提供する GraphQL API を Refine の data provider として扱うための package です。Hasura の権限設定や GraphQL schema を活かしながら、管理画面や内部ツールを構築できます。

## インストール

```sh
npm install @refinedev/hasura
```

## 基本的な使い方

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("HASURA_API_URL", {
  headers: {
    "x-hasura-role": "public",
  },
});

const App = () => {
  return (
    <Refine dataProvider={dataProvider(client)}>
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

Hasura の GraphQL API を使って、CRUD 画面、ダッシュボード、権限つきの業務アプリケーションを素早く作りたい場合に適しています。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine documentation](https://refine.dev/docs/)
- [refine tutorials](https://refine.dev/docs/tutorial/introduction/index/)
