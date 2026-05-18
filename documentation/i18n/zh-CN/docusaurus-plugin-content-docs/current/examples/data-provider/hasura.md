---
id: hasura
title: "Hasura 示例 | Refine v5 中的 REST API 集成"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "在 Refine v5 中实现 Hasura。学习关键步骤，了解 REST、GraphQL 面向自定义 API 和可扩展数据流的扩展方式。"
example-tags: [data-provider, live-provider]
---

任何 REST 或 GraphQL 自定义后端都可以与 Refine 集成。Refine 开箱即用地提供 [Hasura](https://hasura.io/) GraphQL Data Provider。借助 Refine，你可以连接 Hasura 数据库，创建专用查询，并轻松使用数据。本示例详细展示如何在 Refine 项目中使用 Hasura 数据库中的数据。

## ID Data Type

默认情况下，data provider 会假定你的 `ID` 类型为 `uuid`。你可以通过 `idType` 选项更改此行为。你可以将 `Int` 或 `uuid` 作为 `idType` 选项的值，也可以使用函数根据 resource name 判断 `idType`。

#### 将 'Int' 或 'uuid' 传给 `idType`

这会让你为所有 resources 指定 `idType`。

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### 将函数传给 `idType`

这会让你根据 resource name 判断 `idType`。

```tsx
const idTypeMap: Record<string, "Int" | "uuid"> = {
  users: "Int",
  posts: "uuid",
};

const myDataProvider = dataProvider(client, {
  idType: (resource) => idTypeMap[resource] ?? "uuid",
});
```

<CodeSandboxExample path="data-provider-hasura" />
