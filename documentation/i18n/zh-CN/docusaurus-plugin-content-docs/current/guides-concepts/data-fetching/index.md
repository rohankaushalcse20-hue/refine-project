---
title: "数据获取 | Refine v5"
display_title: "数据获取"
sidebar_label: "数据获取"
description: "了解 Refine 如何通过 data providers 和 hooks 将 UI 与 API 连接起来。"
---

在管理型应用中，数据是核心。Refine 通过实现 [`DataProvider`](/core/docs/core/interface-references#dataprovider) 接口的 `dataProvider`，把 UI 连接到一个或多个数据源。

data provider 会接收 `resource`、`id`、`meta` 等信息，并据此调用正确的 API endpoint。

## 数据 hooks

配置好 data provider 后，就可以使用 `useList`、`useOne`、`useCreate`、`useUpdate`、`useDelete` 等 hooks 处理 CRUD 操作。

```tsx
import { useOne } from "@refinedev/core";

const Product = () => {
  const { data, isLoading } = useOne({
    resource: "products",
    id: 1,
  });

  if (isLoading) return <span>Loading...</span>;
  return <pre>{JSON.stringify(data, null, 2)}</pre>;
};
```

## 状态与缓存

这些数据 hooks 底层使用 TanStack Query，因此可以获得 loading、error、success 状态，以及缓存、请求去重、自动 invalidation 和 optimistic update 能力。

## 多 provider 场景

你也可以为不同 resource 指定不同 provider。例如 `posts` 使用 REST，而 `users` 使用 GraphQL，应用层依然可以保持统一的调用方式。
