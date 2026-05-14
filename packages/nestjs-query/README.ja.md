# NestJS Query data provider integration for refine

`@refinedev/nestjs-query` は、nestjs-query を使った GraphQL API を Refine の data provider と live provider に接続する package です。GraphQL の query、mutation、subscription を Refine の resource 操作に対応させられます。

## インストール

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## 基本的な使い方

```tsx
import dataProvider, {
  GraphQLClient,
  liveProvider,
} from "@refinedev/nestjs-query";

import { createClient } from "graphql-ws";

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider(new GraphQLClient("API_URL"))}
      liveProvider={liveProvider(createClient({ url: "WS_URL" }))}
    >
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

nestjs-query で構築した GraphQL backend を使い、リアルタイム更新を含む CRUD 画面を Refine で実装したい場合に適しています。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine NestJS Query example](https://refine.dev/docs/examples/data-provider/nestjs-query/)
- [refine documentation](https://refine.dev/docs/)
