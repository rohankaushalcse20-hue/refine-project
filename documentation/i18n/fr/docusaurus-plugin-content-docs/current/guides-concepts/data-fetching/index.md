---
title: "Data fetching | Refine v5"
display_title: "Data fetching"
sidebar_label: "Data fetching"
description: "Comprenez comment Refine connecte les data providers, hooks et resources pour lire et modifier des données."
---

Dans une application Refine, les écrans sont reliés aux APIs grâce au `dataProvider`. Ce provider expose une interface standard que les hooks de données utilisent pour lister, afficher, créer, mettre à jour et supprimer des enregistrements.

## Data provider

Un `dataProvider` traduit les opérations Refine vers votre backend. Il peut utiliser REST, GraphQL, Supabase, Hasura, Appwrite ou un service interne.

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/simple-rest";

export const App = () => (
  <Refine dataProvider={dataProvider("https://api.fake-rest.refine.dev")} />
);
```

Chaque méthode reçoit des informations comme `resource`, `id`, `pagination`, `filters`, `sorters` et `meta`. Le provider décide ensuite comment les convertir en requête HTTP ou GraphQL.

## Hooks de données

Les hooks comme `useList`, `useOne`, `useMany`, `useCreate`, `useUpdate` et `useDelete` encapsulent les requêtes, le cache, les états de chargement et les erreurs.

```tsx
const { data, isLoading } = useList({
  resource: "products",
});
```

## Filtres, tris et pagination

Les hooks transmettent les filtres, tris et paramètres de pagination au `dataProvider`. Cela garde la logique de l'UI simple tout en laissant au backend la responsabilité d'interpréter les règles exactes.

## Plusieurs providers

Refine peut utiliser plusieurs data providers dans une même application. C'est utile lorsqu'une partie des resources vient d'une API interne et qu'une autre partie vient d'un service externe.

## Relations

Les relations se composent avec les hooks. Par exemple, une liste de produits peut charger ses catégories avec `useMany`, puis afficher les informations associées sans coupler la table à une API précise.
