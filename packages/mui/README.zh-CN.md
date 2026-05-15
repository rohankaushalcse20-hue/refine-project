# refine 的 Material UI 集成

`@refinedev/mui` 将 refine 与 [Material UI](https://mui.com/material-ui/getting-started/) 集成。使用这个包可以通过 Material UI 组件和 refine 的 headless 逻辑构建内部工具、仪表盘和管理后台。

## 安装

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## 快速开始

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

## 文档

- 查看 refine 的 [Material UI 文档](https://refine.dev/docs/ui-integrations/material-ui/introduction)。
- 阅读完整的 [refine 教程](https://refine.dev/tutorial)。
