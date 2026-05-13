---
title: "Tables | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "Maak lijstweergaven met sorting, filtering, pagination en table-integraties."
displayed_sidebar: mainSidebar
slug: /guides-concepts/tables
---

Tabellen zijn de standaardweergave voor veel CRUD-applicaties. Refine helpt bij het verbinden van table state met `getList`, zodat pagination, filters en sorters synchroon blijven met de backend.

## Table hooks

UI-integraties bieden hooks zoals `useTable`, `useDataGrid` of vergelijkbare helpers. Ze leveren props aan je tablecomponent en gebruiken intern de `dataProvider`.

```tsx
const { tableProps } = useTable({
  resource: "products",
});
```

## Filtering en sorting

Filters en sorters worden doorgegeven aan `getList`. De provider bepaalt hoe die informatie wordt vertaald naar queryparameters of een ander API-formaat.

## URL-synchronisatie

Voor lijstpagina's is het vaak handig om table state in de URL te bewaren. Daarmee blijven filters deelbaar, werken refreshes voorspelbaar en kan een gebruiker terugnavigeren naar dezelfde lijststatus.

## Acties per rij

Koppel row actions zoals bekijken, bewerken, klonen of verwijderen aan de resourceconfiguratie. Zo blijven navigatie en permissies consistent met de rest van de applicatie.
