# Refine REST data provider

`@refinedev/rest` は、REST API を Refine の data provider として扱うための package です。独自 backend や REST ベースのサービスを Refine の CRUD フローに接続する出発点になります。

## インストール

```sh
npm install @refinedev/rest
```

## 基本的な使い方

```tsx
import dataProvider from "@refinedev/rest";

const App = () => {
  return (
    <Refine dataProvider={dataProvider("API_URL")}>
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

REST endpoint を持つ backend に対して、list、create、update、delete などの Refine resource 操作を接続したい場合に使います。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [Refine rest docs](https://refine.dev/docs/packages/documentation/data-providers/rest/)
- [refine documentation](https://refine.dev/docs/)
