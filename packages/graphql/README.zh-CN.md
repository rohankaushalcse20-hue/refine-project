# refine 的 GraphQL 集成

`@refinedev/graphql` 为 [GraphQL](https://graphql.org/) API 提供 data provider。它将 refine 的数据契约连接到 `GraphQLClient`，让列表、详情、创建、编辑和删除保持在框架的 CRUD 流程中。

## 安装

```sh
npm install @refinedev/graphql
```

## 基本用法

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

## 文档

- 查看 refine 的 [data provider 文档](https://refine.dev/docs/core/providers/data-provider)。
- 阅读 refine 的 [GraphQL 文档](https://refine.dev/docs/packages/documentation/data-providers/graphql/)。
