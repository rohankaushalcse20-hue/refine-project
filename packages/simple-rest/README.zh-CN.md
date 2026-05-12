# Simple REST data provider

`@refinedev/simple-rest` 是一个面向结构稳定 REST API 的 data provider。它以类似 `json-server` 的接口风格为基础，把 Refine 的 resources 映射到 HTTP endpoints。

## 安装

```sh
npm install @refinedev/simple-rest
```

## 基本用法

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

当 backend 提供标准的列表、创建、更新、删除 endpoints 时，这个 provider 会非常适合。如果你需要 custom headers 或特殊参数，也可以通过封装再做扩展。
