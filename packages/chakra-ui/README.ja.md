# Refine の Chakra UI 連携

`@refinedev/chakra-ui` は、[Chakra UI](https://chakra-ui.com/) を refine アプリケーションの表示レイヤーとして使うためのコンポーネントと hooks を提供します。

## インストール

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## クイックスタート

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/chakra-ui";
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

Chakra UI のアクセシブルでテーマ化しやすいコンポーネントを使いながら、CRUD の data provider や routing は refine の流れに合わせて構築できます。

## ドキュメント

- [refine の Chakra UI ドキュメント](https://refine.dev/docs/ui-integrations/chakra-ui/introduction)を参照してください。
- [refine のチュートリアル](https://refine.dev/docs/tutorial/introduction/index/)も確認できます。
