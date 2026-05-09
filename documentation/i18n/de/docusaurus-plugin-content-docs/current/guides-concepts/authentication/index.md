---
title: "Authentifizierung | Refine v5"
display_title: "Authentifizierung"
sidebar_label: "Authentifizierung"
description: "Implementiere mit dem Auth Provider von Refine Login, Logout, Registrierung und Session-Pruefungen."
---

Authentifizierung bestaetigt die Identitaet eines Users oder Clients. In internen Tools und Dashboards ist sie entscheidend, um Seiten und sensible Daten zu schuetzen.

Refine verwendet dafuer ein `authProvider`-Objekt. Es stellt asynchrone Methoden fuer Login, Logout, Registrierung, Session-Pruefung, Fehlerbehandlung, Identity und Berechtigungen bereit.

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

Fuer geschuetzte Routen und Screens nutzt du APIs wie `useLogin`, `useLogout`, `useRegister`, `useIsAuthenticated`, `useGetIdentity` und `<Authenticated />`.
