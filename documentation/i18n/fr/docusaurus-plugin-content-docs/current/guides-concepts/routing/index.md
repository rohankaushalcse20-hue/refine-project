---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Utilisez React Router, Next.js, Remix ou un router personnalisé avec les resources et hooks Refine."
---

Le routing est essentiel dans une application CRUD. Refine reste agnostique au router : vous définissez les routes comme dans votre framework, puis vous fournissez un `routerProvider` à `<Refine />`.

## Intégrations router

Refine propose des intégrations pour **React Router**, **Next.js** et **Remix**. Elles ajoutent l'inférence de paramètres, les redirections après mutation ou authentification, ainsi que des hooks de navigation.

```tsx title="App.tsx"
import { BrowserRouter, Routes } from "react-router";
import routerProvider from "@refinedev/react-router";

const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* Vos routes */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

Avec Next.js, les routes restent dans `pages` ou `app`. Avec Remix, elles restent dans `app/routes`. Refine n'impose pas une structure de dossiers supplémentaire.

## Resources et routes

Une resource indique à Refine quelles routes correspondent aux actions CRUD.

```tsx
<Refine
  resources={[
    {
      name: "products",
      list: "/products",
      show: "/products/:id",
      create: "/products/new",
      edit: "/products/:id/edit",
    },
  ]}
/>
```

Quand une route correspond à cette définition, des hooks comme `useShow`, `useForm` ou `useTable` peuvent inférer `resource`, `action` et `id`.

## Navigation et redirections

Les hooks `useGo`, `useBack`, `useNavigation` et `useParsed` fournissent une API stable au-dessus du router choisi. Les mutations peuvent rediriger vers `list`, `show`, `edit` ou rester sur la page courante selon la configuration.

## Synchronisation avec l'URL

Le routing peut aussi stocker les états de table ou de formulaire dans l'URL. Cela permet de partager un lien contenant filtres, tris, pagination ou contexte de navigation.
