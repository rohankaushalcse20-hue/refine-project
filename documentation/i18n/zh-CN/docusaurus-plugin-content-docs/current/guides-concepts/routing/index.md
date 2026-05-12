---
title: "Routing | Refine v5"
display_title: "路由"
sidebar_label: "路由"
description: "说明如何在 Refine 中结合 React Router、Next.js 与 Remix 配置 routing。"
---

routing 是 CRUD 应用的核心。由于 Refine 采用 headless 架构，你不会被锁定在特定 framework 中，可以按项目需求选择自己的路由方案。

Refine 为 **React Router**、**Next.js** 和 **Remix** 提供现成集成，并带来以下好处：

- hooks 与 components 可以自动推断参数
- mutation 或认证状态变化后可自动重定向
- 提供 navigation、breadcrumbs 和菜单生成相关工具

Refine 本身是 router-agnostic 的，因此实际的 route 定义仍由应用自己维护。React Router 使用 `Routes`，Next.js 使用 `pages` 或 `app`，Remix 则使用 `app/routes` 目录。

## 集成 router provider

导入目标路由集成包，并将它传给 `<Refine />` 的 `routerProvider`。

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Routes } from "react-router";

export const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* Your route definitions */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

## 建议

保持 routes 与 resources 的映射关系清晰，统一命名约定，并尽量让 `resource`、`id` 等参数通过 router 自动传递给 hooks。
