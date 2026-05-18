---
id: hasura
title: "Esempio Hasura | Integrazione REST API in Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Implementa Hasura in Refine v5. Impara i passaggi chiave per scalare REST e GraphQL per API personalizzate e flussi dati scalabili."
example-tags: [data-provider, live-provider]
---

Qualsiasi backend REST o GraphQL personalizzato può essere integrato con Refine. Refine include il Data Provider GraphQL per [Hasura](https://hasura.io/) pronto all'uso. Grazie a Refine, puoi collegarti al database Hasura, creare query specifiche e usare facilmente i tuoi dati. Questo esempio mostra in dettaglio come usare i dati del database Hasura in un progetto Refine.

## Tipo dati ID

Per impostazione predefinita, il data provider assume che il tipo di `ID` sia `uuid`; puoi modificare questo comportamento usando l'opzione `idType`. Puoi passare `Int` o `uuid` come valore dell'opzione `idType`, oppure usare una funzione per determinare `idType` in base al nome della risorsa.

#### Passare 'Int' o 'uuid' a `idType`

Questo consente di determinare `idType` per tutte le risorse.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### Passare una funzione a `idType`

Questo consente di determinare `idType` in base al nome della risorsa.

```tsx
const idTypeMap: Record<string, "Int" | "uuid"> = {
  users: "Int",
  posts: "uuid",
};

const myDataProvider = dataProvider(client, {
  idType: (resource) => idTypeMap[resource] ?? "uuid",
});
```

<CodeSandboxExample path="data-provider-hasura" />
