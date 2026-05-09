---
title: "Tabellen und Listen | Refine v5"
display_title: "Tabellen"
sidebar_label: "Tabellen"
description: "Erstelle mit Refine Tabellen, Listen, Filter, Sortierung und Pagination."
---

Tabellen und Listen machen API-Daten in der UI nutzbar. Refine liefert Hooks, die Pagination, Filter, Sortierung und Loading-Status mit dem Data Provider verbinden.

## Listen

`useTable` und `useList` sind die Grundlagen fuer Listenansichten mit UI-Integrationen oder eigenen Komponenten.

```tsx
const table = useTable({
  resource: "products",
  pagination: { pageSize: 10 },
});
```

## Filter und Sortierung

Filter und Sorter werden in Parameter umgewandelt, die dein Data Provider an die API weitergibt. Dadurch bleibt die Backend-Kommunikation sauber von der UI getrennt.

## CRUD-Aktionen

Listen koennen direkt mit Create-, Edit-, Show- und Delete-Aktionen verknuepft werden. Dabei lassen sich sowohl Berechtigungen als auch i18n-Labels beruecksichtigen.
