---
title: "Tables et listes | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "Construisez tables, listes, filtres, tri et pagination avec Refine."
---

Les tables et listes transforment les données d'une API en interfaces explorables. Refine fournit des hooks pour connecter pagination, filtres, tri et états de chargement au data provider.

## Listes

`useTable` et `useList` sont les bases pour construire des listes avec une UI integration ou des composants maison.

```tsx
const table = useTable({
  resource: "products",
  pagination: { pageSize: 10 },
});
```

## Filtres et tri

Les filtres et sorters deviennent des paramètres que le data provider peut envoyer à l'API. La communication backend reste découplée de l'interface.

## Actions CRUD

Associez les listes aux actions créer, modifier, afficher et supprimer. Les actions peuvent respecter les permissions et traduire les labels avec i18n.
