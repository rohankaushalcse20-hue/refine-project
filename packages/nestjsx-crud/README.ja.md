# NestJSX CRUD data provider integration for refine

`@refinedev/nestjsx-crud` は、NestJSX CRUD 形式の REST API を Refine の data provider として扱うための package です。NestJS で構築した CRUD backend を Refine の resource 操作に接続できます。

## インストール

```sh
npm install @refinedev/nestjsx-crud
```

## 基本的な使い方

```tsx
import dataProvider from "@refinedev/nestjsx-crud";

const App = () => {
  return (
    <Refine dataProvider={dataProvider("API_URL")}>
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

NestJSX CRUD の規約に沿った endpoint を既に持っており、Refine 側で一覧、詳細、作成、編集の UI を素早く作りたい場合に使います。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine NestJS CRUD example](https://refine.dev/docs/examples/data-provider/nestjsxCrud/)
- [refine documentation](https://refine.dev/docs/)
