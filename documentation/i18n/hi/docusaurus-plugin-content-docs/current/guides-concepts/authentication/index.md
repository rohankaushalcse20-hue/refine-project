---
title: "Authentication | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "Refine के auth provider के साथ login, logout, register और session checks लागू करें।"
---

Authentication किसी user या client की पहचान सत्यापित करता है। Internal tools और dashboards में यह pages और sensitive data को सुरक्षित रखने के लिए महत्वपूर्ण है।

Refine `authProvider` का उपयोग करता है। यह object login, logout, register, session check, error handling, identity और permissions के लिए async methods देता है।

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

Routes और protected screens के लिए `useLogin`, `useLogout`, `useRegister`, `useIsAuthenticated`, `useGetIdentity` और `<Authenticated />` जैसे APIs का उपयोग करें।
