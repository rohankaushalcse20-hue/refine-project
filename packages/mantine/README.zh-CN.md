# refine 的 Mantine 集成

`@refinedev/mantine` 提供组件和 hooks，可使用 [Mantine](https://mantine.dev/) 构建 refine 界面。它把布局、表单、通知和表格集成到 refine 的 headless 流程中。

## 安装

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## 快速开始

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

## 文档

- 查看 refine 的 [Mantine 文档](https://refine.dev/docs/ui-integrations/mantine/introduction)。
- 阅读 [refine 教程](https://refine.dev/docs/tutorial/introduction/index/)。
