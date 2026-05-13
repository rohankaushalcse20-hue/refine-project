---
title: "Data Fetching | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "Gebruik data providers en Refine hooks om consistente CRUD-verzoeken naar je backend te sturen."
displayed_sidebar: mainSidebar
slug: /guides-concepts/data-fetching
---

Data fetching in Refine draait om het `dataProvider`-contract. De provider vertaalt generieke CRUD-acties naar de API van jouw backend, terwijl Refine hooks een consistente interface geven aan je pagina's.

## Data provider

Een `dataProvider` bevat methoden zoals `getList`, `getOne`, `create`, `update`, `deleteOne` en `custom`. Deze methoden krijgen resource-informatie, filters, sorters, pagination en metadata mee.

```tsx
<Refine
  dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
  resources={[
    {
      name: "products",
      list: "/products",
    },
  ]}
/>
```

## Hooks

Hooks zoals `useList`, `useOne`, `useCreate`, `useUpdate` en `useDelete` roepen de provider aan. Ze bouwen voort op React Query, waardoor caching, loading states, retries en invalidation op een voorspelbare manier werken.

## Filters, sorters en pagination

Lijstpagina's sturen filters, sorters en pagination door naar `getList`. Je provider bepaalt hoe die velden worden omgezet naar queryparameters, GraphQL-variabelen of een ander backendprotocol.

## Fouten en metadata

Gebruik `meta` voor provider-specifieke informatie, zoals extra headers, GraphQL fields of embedded relations. Fouten kunnen via React Query en `notificationProvider` worden afgehandeld, zodat gebruikers duidelijke feedback krijgen.
