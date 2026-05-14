---
title: "Authentification | Refine v5"
display_title: "Authentification"
sidebar_label: "Authentification"
description: "Configurez un authProvider Refine et utilisez les hooks d'authentification pour protéger vos pages."
---

L'authentification vérifie l'identité d'un utilisateur ou d'un client. Dans Refine, elle est centralisée par un `authProvider` passé au composant `<Refine />`.

## Auth provider

Un `authProvider` est un objet de méthodes asynchrones comme `login`, `logout`, `check`, `register`, `forgotPassword`, `getPermissions` et `getIdentity`.

```tsx title="App.tsx"
import { Refine, AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  login: async ({ email, password }) => {
    const { status } = handleLogin(email, password);

    if (status === 200) {
      return { success: true, redirectTo: "/dashboard" };
    }

    return {
      success: false,
      error: { name: "Login Error", message: "Invalid credentials" },
    };
  },
  check: async () => ({}),
  logout: async () => ({}),
  onError: async () => ({}),
  register: async () => ({}),
  forgotPassword: async () => ({}),
  updatePassword: async () => ({}),
  getPermissions: async () => ({}),
  getIdentity: async () => ({}),
};

const App = () => <Refine authProvider={authProvider}>...</Refine>;
```

## Hooks et composants

Les hooks `useLogin`, `useLogout`, `useRegister`, `useIsAuthenticated`, `useGetIdentity` et `usePermissions` appellent les méthodes du provider. Le composant `<Authenticated />` protège une section de l'interface et affiche un fallback si l'utilisateur n'a pas accès.

```tsx
import { Authenticated } from "@refinedev/core";

const Page = () => (
  <Authenticated
    loading={<div>loading...</div>}
    fallback={<div>You cannot access this section</div>}
  >
    <h1>Welcome to your dashboard</h1>
  </Authenticated>
);
```

## Données et erreurs

Après connexion, le data provider peut envoyer les credentials dans les requêtes. La méthode `onError` permet aussi de réagir à des erreurs comme un token expiré et de déclencher une redirection ou une déconnexion.
