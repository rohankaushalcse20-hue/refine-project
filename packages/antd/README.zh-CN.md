# refine 的 Ant Design 集成

`@refinedev/antd` 将 refine 的 headless 逻辑与 [Ant Design](https://ant.design/) 的组件、布局、表单、表格和视觉反馈能力结合起来。

## 安装

```sh
npm install @refinedev/antd antd
```

## 快速开始

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

如果你希望交付 Ant Design 界面，同时继续使用 refine 的数据、路由、认证和授权 providers，可以选择这个集成。

## 文档

- 查看 refine 的 [Ant Design 文档](https://refine.dev/docs/ui-integrations/ant-design/introduction)。
- 阅读完整的 [refine 教程](https://refine.dev/tutorial)。
