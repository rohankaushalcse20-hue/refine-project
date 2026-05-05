---
title: "Authentification | Refine v5"
display_title: "Authentification"
sidebar_label: "Authentification"
description: "Implémentez login, logout, inscription et vérification de session avec l'auth provider de Refine."
---

L'authentification vérifie l'identité des utilisateurs ou clients. Dans les outils internes et dashboards, elle protège les pages et les données sensibles.

Refine utilise un `authProvider`. Cet objet contient des méthodes asynchrones pour login, logout, inscription, vérification de session, gestion d'erreurs, identité et permissions.

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

Utilisez `useLogin`, `useLogout`, `useRegister`, `useIsAuthenticated` et `useGetIdentity`, ou le composant `<Authenticated />` pour protéger des routes.
