# Refine の Ant Design 連携

`@refinedev/antd` は refine の headless なロジックに、[Ant Design](https://ant.design/) のコンポーネント、layout、form、table、通知まわりの UI を組み合わせるためのパッケージです。

## インストール

```sh
npm install @refinedev/antd antd
```

## クイックスタート

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/antd";
import dataProvider from "@refinedev/simple-rest";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";

import "antd/dist/reset.css";

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

Ant Design の見た目を使いながら、データ取得、routing、認証、認可などの provider 構成は refine に任せたい場合に使います。

## ドキュメント

- [refine の Ant Design ドキュメント](https://refine.dev/docs/ui-integrations/ant-design/introduction)を参照してください。
- [refine のチュートリアル](https://refine.dev/tutorial)も確認できます。
