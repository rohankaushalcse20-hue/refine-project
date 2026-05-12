---
title: "核心概念 | Refine v5"
display_title: "核心概念"
sidebar_label: "核心概念"
description: "理解 Refine 的 headless 架构、resources、providers、hooks 与 meta 概念。"
---

Refine 是一个用于快速构建 Web 应用的可扩展框架。它以 **hooks**、可插拔的 **providers** 以及稳定的数据和状态管理能力为基础。

## Headless 概念

Refine 不把你限制在某一套预设样式组件里。它提供 `hooks`、`components`、`providers` 和工具函数，同时把业务逻辑与 UI 解耦。

因此你既可以使用自定义设计系统，也可以接入 Tailwind CSS、Ant Design、Material UI、Mantine、Chakra UI，并继续复用 `@refinedev/core` 的能力。

## Resource

**resource** 用来表示应用中的实体，例如 `products`、`blogPosts`、`orders`。resource 定义会把路由、CRUD 操作、菜单和 providers 连接到同一个结构上。

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        show: "/products/:id",
        edit: "/products/:id/edit",
        create: "/products/new",
      },
    ]}
  />
);
```

## Providers

providers 负责数据、认证、授权、通知、i18n、实时更新、routing、审计日志等关键能力。你可以使用内置实现，也可以接入自己写的 provider。

## Hooks

Refine 的 hooks 是 headless 且与具体库无关的。借助 `useGo`、`useCan`、`useTranslate` 等 API，你可以用一致的方式处理跳转、权限和翻译。

## Meta

`meta` 属性可用于向 providers 与 hooks 传递额外信息，例如 headers、特殊参数、字段选择、多租户上下文或 GraphQL 查询提示。
