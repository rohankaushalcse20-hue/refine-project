# refine の TanStack React Table 連携

`@refinedev/react-table` は refine のデータ hooks と [TanStack React Table](https://tanstack.com/table/v8) を接続します。pagination、filter、sorting、resource と同期した状態を持つ headless な table を組み立てやすくします。

## インストール

```sh
npm install @refinedev/react-table @tanstack/react-table
```

## 基本的な使い方

```tsx
import { useTable } from "@refinedev/react-table";

const table = useTable({
  columns,
  refineCoreProps: {
    resource: "posts",
  },
});
```

## いつ使うか

table の markup、styles、components を自分で制御しながら、データ取得と CRUD 状態の管理を refine に任せたい場合に使います。

## ドキュメント

- [refine の TanStack Table ドキュメント](https://refine.dev/docs/packages/documentation/tanstack-table/introduction)を参照してください。
- [TanStack React Table の advanced example](https://refine.dev/docs/examples/table/tanstack/advanced-react-table/)も確認できます。
