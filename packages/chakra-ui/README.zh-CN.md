# refine 的 Chakra UI 集成

`@refinedev/chakra-ui` 提供组件和 hooks，可将 [Chakra UI](https://chakra-ui.com/) 用作 refine 应用的视觉层。

## 安装

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## 快速开始

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

当你希望使用 Chakra UI 的无障碍、模块化、可主题化组件来构建 refine 面板时，可以使用这个集成。

## 文档

- 查看 refine 的 [Chakra UI 文档](https://refine.dev/docs/ui-integrations/chakra-ui/introduction)。
- 阅读 [refine 教程](https://refine.dev/docs/tutorial/introduction/index/)。
