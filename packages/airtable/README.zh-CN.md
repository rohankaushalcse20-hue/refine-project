# refine 的 Airtable 集成

`@refinedev/airtable` 是用于在 refine 应用中使用 [Airtable](https://www.airtable.com/) base 的 data provider。它可以在 Airtable 托管的关系型表之上构建 CRUD 页面，同时不会把应用绑定到特定 UI 库。

## 安装

```sh
npm install @refinedev/airtable
```

## 基本用法

```tsx
import dataProvider from "@refinedev/airtable";

const App = () => (
  <Refine dataProvider={dataProvider("API_KEY", "BASE_ID")}>
    {/* ... */}
  </Refine>
);
```

当 Airtable 是原型、内部运营工具或管理后台的主要数据源时，可以使用这个包。

## 文档

- 阅读 refine 的 [data provider 文档](https://refine.dev/docs/core/providers/data-provider)。
- 查看 refine 的 [Airtable 示例](https://refine.dev/docs/examples/data-provider/airtable/)。
