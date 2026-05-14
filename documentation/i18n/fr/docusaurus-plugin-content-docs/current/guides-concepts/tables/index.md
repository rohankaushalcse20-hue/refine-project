---
title: "Tables | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "Construisez des listes, tableaux et data grids avec useTable, pagination, filtres et tri."
---

Les tables affichent les collections de resources et concentrent souvent la recherche, le tri, la pagination et les actions CRUD.

## useTable

Le hook `useTable` connecte une table à un `dataProvider`. Il gère les données, le chargement, les filtres, les sorters et la pagination, puis expose les propriétés attendues par l'intégration UI.

```tsx
const { tableQuery, current, setCurrent, pageSize, setPageSize } = useTable({
  resource: "products",
});
```

Les intégrations Ant Design, Material UI, Mantine, Chakra UI et TanStack Table adaptent cette logique à leurs composants.

## Pagination

La pagination peut être gérée côté serveur, côté client ou désactivée. En mode serveur, chaque changement de page déclenche une nouvelle requête via le `dataProvider`.

## Filtres et tri

Les filtres et sorters sont représentés par les types Refine `CrudFilters` et `CrudSorting`. Le `dataProvider` les traduit ensuite dans le format attendu par l'API.

## Recherche

`useTable` peut connecter un formulaire de recherche aux filtres avec `onSearch`. Cela permet de garder les champs de recherche dans l'UI tout en envoyant des critères structurés au backend.

## URL et relations

Avec `syncWithLocation`, l'état du tableau peut être encodé dans l'URL. Pour les données liées, composez `useTable` avec `useOne` ou `useMany` afin d'afficher des informations de resources associées.
