# GraphQL data provider

`@refinedev/graphql` は、Refine アプリケーションを独自の GraphQL backend に接続するための data provider です。query、mutation、通信の約束事を自分で設計したい場合の柔軟な土台になります。

## インストール

```sh
npm install @refinedev/graphql
```

## 基本的な使い方

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => {
  return (
    <Refine dataProvider={dataProvider(client)}>
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

backend が GraphQL endpoint を公開しており、Refine の resource、型、検索条件、mutation をプロジェクト固有の GraphQL スキーマに合わせたい場合に使います。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine GraphQL docs](https://refine.dev/docs/packages/documentation/data-providers/graphql/)
- [refine documentation](https://refine.dev/docs/)
