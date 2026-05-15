# Refine の Mantine 連携

`@refinedev/mantine` は、[Mantine](https://mantine.dev/) を使って refine の UI を構築するためのコンポーネントと hooks を提供します。layout、form、notification、table を refine の headless な流れに統合できます。

## インストール

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## クイックスタート

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mantine";
import dataProvider from "@refinedev/simple-rest";
import RouterProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";

export default function App() {
  return (
    <BrowserRouter>
      <Refine
        routerProvider={RouterProvider}
        dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
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

- [refine の Mantine ドキュメント](https://refine.dev/docs/ui-integrations/mantine/introduction)を参照してください。
- [refine のチュートリアル](https://refine.dev/docs/tutorial/introduction/index/)も確認できます。
