---
title: "授权 | Refine v5"
display_title: "授权"
sidebar_label: "授权"
description: "使用 access control provider 控制 actions、routes 与 components 的访问权限。"
---

授权定义的是“已认证用户可以做什么”。在 Refine 中，可以通过 `accessControlProvider` 为 hooks、buttons、menus 和 pages 提供权限判断。

## Access control provider

核心方法是 `can`。它接收 `resource`、`action` 以及附加参数，并返回该操作是否被允许。

```tsx
const accessControlProvider = {
  can: async ({ resource, action }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Only admins can delete posts" };
    }

    return { can: true };
  },
};
```

## 在 components 中使用

可以使用 `useCan` 根据权限动态决定是否渲染 UI。

```tsx
const { data } = useCan({ resource: "posts", action: "delete" });

return data?.can ? <DeleteButton /> : null;
```

## 建议

access control provider 适合改善前端体验，但最终权限校验仍应始终由 backend 负责。
