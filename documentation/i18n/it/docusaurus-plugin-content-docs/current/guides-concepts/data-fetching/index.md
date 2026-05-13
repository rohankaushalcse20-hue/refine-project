---
title: "Data Fetching | Refine v5"
display_title: "Recupero dati"
sidebar_label: "Recupero dati"
description: "Scopri il modello di lettura e scrittura dati di Refine con data provider e query hooks."
---

In Refine l'accesso ai dati è modellato intorno al `dataProvider`. Componenti UI e hooks leggono e scrivono dati tramite metodi CRUD comuni, senza conoscere i dettagli del backend.

## Data provider

Il `dataProvider` è l'adattatore che collega la tua API a Refine. Metodi come `getList`, `getOne`, `create`, `update`, `deleteOne` e altri portano backend diversi sotto lo stesso contratto.

```ts title=dataProvider.ts
export const dataProvider = {
  getList: async ({ resource, pagination, filters, sorters }) => {
    // Implementa qui la richiesta API.
  },
  getOne: async ({ resource, id }) => {
    // Recupera qui un singolo record.
  },
};
```

## Query hooks

Hooks come `useList`, `useOne`, `useMany`, `useCreate`, `useUpdate` e `useDelete` chiamano i metodi del data provider. Refine gestisce cache, loading state, error handling e invalidation.

## Liste

Nelle pagine lista, pagination, sorting e filtering vengono passati a `getList`. In questo modo il comportamento di tabelle e liste resta coerente con le query backend.

## Mutations

Le operazioni create, update e delete si eseguono con mutation hooks. Refine supporta mutation mode come `pessimistic`, `optimistic` e `undoable`, così puoi bilanciare esperienza utente e coerenza dei dati.

## Error handling

Quando i metodi del provider restituiscono errori, Refine li espone tramite hooks e integrazioni di notification. Se il formato della tua API è diverso, puoi normalizzare gli errori nel provider.
