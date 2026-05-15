# refine 的 Medusa 集成

`@refinedev/medusa` 将 refine 应用连接到 [Medusa](https://medusajs.com/) 后端，用于构建电商体验。该包提供 data provider 和 auth provider，便于搭建管理后台与运营工具。

## 安装

```sh
npm install @refinedev/medusa
```

## 基本用法

```tsx
import dataProvider, { authProvider } from "@refinedev/medusa";

const App = () => (
  <Refine
    dataProvider={dataProvider("API_URL")}
    authProvider={authProvider("API_URL")}
  >
    {/* ... */}
  </Refine>
);
```

## 文档

- 查看 refine 的 [data provider 文档](https://refine.dev/docs/core/providers/data-provider)。
- 阅读 [refine 教程](https://refine.dev/docs/tutorial/introduction/index/)。
