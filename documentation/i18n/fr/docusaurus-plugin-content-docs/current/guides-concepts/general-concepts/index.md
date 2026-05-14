---
title: "Concepts généraux | Refine v5"
display_title: "Concepts généraux"
sidebar_label: "Concepts généraux"
description: "Apprenez les bases de Refine : architecture headless, resources, providers, hooks et meta."
---

Refine est un framework extensible pour créer rapidement des applications web. Son architecture moderne repose sur des **hooks**, un système de **providers** connectables et une gestion robuste des données.

## Concept headless

Refine n'impose pas une bibliothèque de composants visuels. Il fournit plutôt des `hooks`, `components`, `providers` et utilitaires qui séparent la logique métier de l'interface.

Cette séparation permet d'utiliser vos propres designs ou des frameworks UI comme Tailwind CSS, Ant Design, Material UI, Mantine et Chakra UI tout en conservant les avantages de `@refinedev/core`.

## Resource

Une **resource** représente une entité de l'application, par exemple `products`, `blogPosts` ou `orders`. Sa définition relie routes, opérations CRUD, menus et providers de manière structurée.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        show: "/products/:id",
        edit: "/products/:id/edit",
        create: "/products/new",
      },
    ]}
  />
);
```

## Providers

Les providers gèrent les zones clés : données, authentification, autorisation, notifications, i18n, temps réel, routing et audit logs. Vous pouvez utiliser les providers fournis ou créer les vôtres pour adapter Refine à votre API et à vos règles métier.

## Hooks

Les hooks Refine sont headless et indépendants de la bibliothèque UI. Par exemple, `useGo` navigue quel que soit le router, `useCan` interroge l'access control provider et `useTranslate` accède au provider i18n.

## Meta

La propriété `meta` transmet des informations supplémentaires aux providers et hooks. Elle sert pour les headers, paramètres spéciaux, sélections de champs, scénarios multi-tenant ou génération de requêtes GraphQL.
