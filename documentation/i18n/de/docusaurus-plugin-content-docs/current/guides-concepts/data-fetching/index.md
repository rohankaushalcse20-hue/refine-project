---
title: "Data Fetching | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "Lerne, wie Refine ueber Data Provider und Hooks die UI mit APIs verbindet."
---

Daten stehen im Zentrum fast jeder Admin-Anwendung. Refine verbindet die UI ueber einen `dataProvider` mit einer oder mehreren Datenquellen. Dieser implementiert das [`DataProvider`](/core/docs/core/interface-references#dataprovider)-Interface.

Der Data Provider erhaelt Informationen wie `resource`, `id` und `meta` und entscheidet dann, mit welchem Endpoint oder welcher Query die eigentliche Datenquelle angesprochen wird.

## Data Hooks

Sobald der Provider registriert ist, kannst du CRUD-Aktionen mit Hooks wie `useList`, `useOne`, `useCreate`, `useUpdate` und `useDelete` ausfuehren.

```tsx
import { useOne } from "@refinedev/core";

const Product = () => {
  const { data, isLoading } = useOne({ resource: "products", id: 1 });
  if (isLoading) return <span>Loading...</span>;
  return <pre>{JSON.stringify(data, null, 2)}</pre>;
};
```

## Status und Cache

Die Data Hooks nutzen TanStack Query fuer Loading- und Error-Status, Caching, Request-Deduplizierung, Invalidation und optimistische Updates.

## Mehrere Provider

Du kannst fuer ein Resource REST und fuer ein anderes GraphQL verwenden, ohne dass sich die API in deinen Komponenten aendert.
