# refine 的 Hasura 集成

`@refinedev/hasura` 通过 GraphQL 将 refine 应用连接到 [Hasura](https://hasura.io/)。当 Hasura 为你的数据生成 API，而 refine 负责 CRUD 页面时，可以使用这个包。

## 安装

```sh
npm install @refinedev/hasura
```

## 基本用法

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("HASURA_API_URL", {
  headers: {
    "x-hasura-role": "public",
  },
});

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

## 文档

- 查看 refine 的 [data provider 文档](https://refine.dev/docs/core/providers/data-provider)。
- 阅读 [refine 教程](https://refine.dev/docs/tutorial/introduction/index/)。
