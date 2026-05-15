# Integrazione GraphQL per refine

`@refinedev/graphql` fornisce un data provider per collegare refine ad API [GraphQL](https://graphql.org/) mantenendo il modello CRUD basato su resources.

## Installazione

```sh
npm install @refinedev/graphql graphql-request
```

## Uso di base

Configura il client GraphQL e passa il provider a `Refine` come `dataProvider`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/graphql";
```

Il pacchetto aiuta a mappare query e mutation GraphQL sulle operazioni di data fetching usate dagli hooks di refine.

## Documentazione

- Consulta la [documentazione del provider GraphQL](https://refine.dev/docs/data/packages/graphql/).
- Per il linguaggio e il runtime, consulta la [documentazione GraphQL](https://graphql.org/learn/).
