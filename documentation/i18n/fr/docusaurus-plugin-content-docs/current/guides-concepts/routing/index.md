---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Configurez le routing dans Refine avec React Router, Next.js, Remix ou une solution compatible."
---

Le routing est essentiel dans une application CRUD. L'architecture headless de Refine permet d'utiliser la solution de routes de votre choix sans être lié à un framework spécifique.

Refine inclut des intégrations pour **React Router**, **Next.js** et **Remix**. Elles facilitent la détection automatique des paramètres, les redirections après mutation ou authentification et les utilitaires de navigation.

Comme Refine reste agnostique du router, vous continuez à définir les routes de votre application. Avec React Router, elles vivent dans `Routes`; avec Next.js, dans `pages` ou `app`; avec Remix, dans `app/routes`.

## Intégrer un router provider

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Routes } from "react-router";

export const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* vos routes */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

Gardez les routes alignées avec vos resources et laissez les hooks recevoir `resource`, `id` et les autres paramètres depuis le router lorsque c'est possible.
