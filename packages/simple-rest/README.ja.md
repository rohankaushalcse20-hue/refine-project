# Simple REST data provider

`@refinedev/simple-rest` は、構造が標準化された REST API 向けの data provider です。`json-server` に近いスタイルを前提に、Refine の resources を HTTP endpoints へ接続します。

## インストール

```sh
npm install @refinedev/simple-rest
```

## 基本的な使い方

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

backend が一覧、作成、更新、削除のためのシンプルな REST endpoints を提供している場合に適しています。custom headers や特別なパラメータが必要であれば、wrapper を作るか拡張して使えます。
