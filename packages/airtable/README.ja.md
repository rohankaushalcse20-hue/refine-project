# Airtable integration for refine

`@refinedev/airtable` は、Airtable base を Refine の data provider として利用するための package です。Airtable のテーブルを resource として扱い、内部向けの編集画面や管理画面を作れます。

## インストール

```sh
npm install @refinedev/airtable
```

## 基本的な使い方

```tsx
import dataProvider from "@refinedev/airtable";

const App = () => {
  return (
    <Refine dataProvider={dataProvider("API_KEY", "BASE_ID")}>
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

Airtable で管理しているデータに対して、Refine の list、show、create、edit 画面を用意したい場合に適しています。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine Airtable example](https://refine.dev/docs/examples/data-provider/airtable/)
- [refine documentation](https://refine.dev/docs/)
