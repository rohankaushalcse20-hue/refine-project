---
title: "인증 | Refine v5"
display_title: "인증"
sidebar_label: "인증"
description: "Refine의 auth provider로 login, logout, 회원가입, 세션 확인 흐름을 구현합니다."
---

인증은 사용자나 클라이언트의 신원을 확인하는 과정입니다. 내부 도구, 대시보드, 관리자 패널에서는 페이지와 데이터를 보호하기 위한 핵심 요소입니다.

Refine는 `authProvider`를 통해 인증을 처리합니다. 이 객체에는 login, logout, 회원가입, 세션 확인, 오류 처리, identity 및 permissions 조회를 위한 비동기 메서드를 구현합니다.

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

## 인증 hooks

Refine는 `useLogin`, `useLogout`, `useRegister`, `useIsAuthenticated`, `useGetIdentity` 같은 hooks를 제공합니다. `<Authenticated />` component를 사용하면 라우트 보호나 조건부 렌더링도 쉽게 구현할 수 있습니다.

## 통합

자체 인증 흐름을 만들 수도 있고, Google, Auth0, Amazon Cognito, Okta 같은 provider를 통합할 수도 있습니다.
