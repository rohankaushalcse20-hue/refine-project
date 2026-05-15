# Refine の Material UI 連携

`@refinedev/mui` は refine と [Material UI](https://mui.com/material-ui/getting-started/) を統合します。Material UI のコンポーネントと refine の headless なロジックを組み合わせて、社内ツール、dashboard、管理画面を構築できます。

## インストール

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## クイックスタート

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mui";
import dataProvider from "@refinedev/simple-rest";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";

export default function App() {
  return (
    <BrowserRouter>
      <Refine
        dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
        routerProvider={routerProvider}
        resources={[{ name: "products", list: "/products" }]}
      >
        <Routes>
          <Route element={<ThemedLayoutV2><Outlet /></ThemedLayoutV2>}>
            <Route path="/products">
              <Route index element={<ProductList />} />
            </Route>
          </Route>
        </Routes>
      </Refine>
    </BrowserRouter>
  );
}
```

## ドキュメント

- [refine の Material UI ドキュメント](https://refine.dev/docs/ui-integrations/material-ui/introduction)を参照してください。
- [refine のチュートリアル](https://refine.dev/tutorial)も確認できます。
