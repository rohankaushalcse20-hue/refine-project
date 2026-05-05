---
title: "Data Fetching | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "Découvrez comment Refine connecte l'interface aux APIs avec data providers et hooks."
---

Les données sont au centre d'une application d'administration. Refine connecte l'UI à une ou plusieurs sources via un `dataProvider` qui implémente l'interface [`DataProvider`](/core/docs/core/interface-references#dataprovider).

Le data provider reçoit le `resource`, l'`id` et `meta`, puis appelle l'endpoint adapté de votre API.

## Hooks de données

Après avoir enregistré un data provider, utilisez `useList`, `useOne`, `useCreate`, `useUpdate` et `useDelete` pour gérer les opérations CRUD.

```tsx
import { useOne } from "@refinedev/core";

const Product = () => {
  const { data, isLoading } = useOne({ resource: "products", id: 1 });
  if (isLoading) return <span>Loading...</span>;
  return <pre>{JSON.stringify(data, null, 2)}</pre>;
};
```

## État et cache

Les hooks s'appuient sur TanStack Query pour les états de chargement, d'erreur et de succès, le cache, la déduplication, l'invalidation et les mises à jour optimistes.

## Plusieurs providers

Vous pouvez utiliser REST pour un resource et GraphQL pour un autre tout en gardant une API cohérente côté composants.
