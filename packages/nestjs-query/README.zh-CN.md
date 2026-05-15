# refine 的 NestJS Query 集成

`@refinedev/nestjs-query` 将 refine 连接到使用 [NestJS Query](https://doug-martin.github.io/nestjs-query/docs) 构建的 API。它提供 GraphQL data provider，并通过 `graphql-ws` 支持实时事件。

## 安装

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## 基本用法

```tsx
import dataProvider, {
  GraphQLClient,
  liveProvider,
} from "@refinedev/nestjs-query";
import { createClient } from "graphql-ws";

const App = () => (
  <Refine
    dataProvider={dataProvider(new GraphQLClient("API_URL"))}
    liveProvider={liveProvider(createClient({ url: "WS_URL" }))}
  >
    {/* ... */}
  </Refine>
);
```

## 文档

- 查看 refine 的 [data provider 文档](https://refine.dev/docs/core/providers/data-provider)。
- 查看 refine 的 [NestJS Query 示例](https://refine.dev/docs/examples/data-provider/nestjs-query/)。
