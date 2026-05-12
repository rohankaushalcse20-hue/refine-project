---
title: "认证 | Refine v5"
display_title: "认证"
sidebar_label: "认证"
description: "通过 Refine 的 auth provider 实现 login、logout、注册与会话检查流程。"
---

认证用于验证用户或客户端身份，是内部工具、仪表盘和管理后台中保护页面与数据的关键能力。

Refine 通过 `authProvider` 处理认证。这个对象通常包含 login、logout、注册、会话检查、错误处理以及 identity、permissions 查询等异步方法。

## Auth provider

```tsx title="auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  login: async ({ email, password }) => {
    const isValid = email && password;
    return isValid
      ? { success: true, redirectTo: "/dashboard" }
      : { success: false, error: { name: "LoginError", message: "Invalid credentials" } };
  },
  check: async () => ({ authenticated: true }),
  logout: async () => ({ success: true, redirectTo: "/login" }),
  onError: async () => ({}),
};
```

## 认证 hooks

Refine 提供 `useLogin`、`useLogout`、`useRegister`、`useIsAuthenticated`、`useGetIdentity` 等 hooks。借助 `<Authenticated />` component，也可以轻松实现路由保护或条件渲染。

## 集成方式

你既可以实现自己的认证流程，也可以接入 Google、Auth0、Amazon Cognito、Okta 等 provider。
