---
title: "Autenticação | Refine v5"
display_title: "Autenticação"
sidebar_label: "Autenticação"
description: "Implemente login, logout, cadastro e verificação de sessão com o auth provider do Refine."
---

A autenticação confirma a identidade do usuário ou do cliente. Em ferramentas internas e dashboards, ela é essencial para proteger páginas e dados sensíveis.

O Refine usa um objeto `authProvider` para isso. Ele expõe métodos assíncronos para login, logout, cadastro, verificação de sessão, tratamento de erros, identidade e permissões.

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

Para proteger rotas e telas, use APIs como `useLogin`, `useLogout`, `useRegister`, `useIsAuthenticated`, `useGetIdentity` e `<Authenticated />`.
