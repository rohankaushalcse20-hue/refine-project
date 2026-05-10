---
title: "認証 | Refine v5"
display_title: "認証"
sidebar_label: "認証"
description: "Refine の auth provider を使って login、logout、登録、セッション確認を実装します。"
---

認証は、ユーザーやクライアントの身元を確認するための仕組みです。社内ツール、ダッシュボード、管理画面では、ページやデータを保護するための重要な要素になります。

Refine では `authProvider` によって認証を扱います。このオブジェクトには、login、logout、登録、セッション確認、エラー処理、identity や permissions の取得のための非同期メソッドを実装します。

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

## 認証用 hooks

Refine は `useLogin`、`useLogout`、`useRegister`、`useIsAuthenticated`、`useGetIdentity` などの hooks を提供します。`<Authenticated />` component を使ってルート保護や条件付きレンダリングも行えます。

## 統合

独自の認証フローを組み立てることも、Google、Auth0、Amazon Cognito、Okta などの provider を組み込むことも可能です。
