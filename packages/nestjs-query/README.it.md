# Integrazione NestJS Query per refine

`@refinedev/nestjs-query` fornisce un data provider per collegare refine ad API create con [Nestjs-query](https://doug-martin.github.io/nestjs-query/docs).

## Installazione

```sh
npm install @refinedev/nestjs-query graphql-ws
```

## Uso di base

Configura il client GraphQL verso il backend NestJS Query e passa il provider a `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/nestjs-query";
```

Il provider mappa le operazioni CRUD di refine sulle query e mutation generate dal backend NestJS Query.

## Documentazione

- Consulta la [documentazione NestJS Query di refine](https://refine.dev/docs/data/packages/nestjs-query/).
- Per il backend, consulta la [documentazione Nestjs-query](https://doug-martin.github.io/nestjs-query/docs/introduction/getting-started/).
