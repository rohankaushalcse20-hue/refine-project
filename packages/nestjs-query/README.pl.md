# Integracja NestJS Query dla Refine

`@refinedev/nestjs-query` udostępnia data provider dla API zbudowanych z [NestJS Query](https://doug-martin.github.io/nestjs-query/docs). Pakiet łączy schemat GraphQL backendu ze standardowymi hookami CRUD Refine.

## Instalacja

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## Podstawowe użycie

Skonfiguruj GraphQL endpoint i przekaż provider do `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/nestjs-query";
```

Po podłączeniu resources Refine mogą korzystać z filtrowania, sortowania, paginacji i mutacji przez API NestJS Query.

## Dokumentacja

- Otwórz [dokumentację NestJS Query data provider](https://refine.dev/docs/data/packages/nestjs-query/).
- Więcej o bibliotece backendowej znajdziesz w [dokumentacji NestJS Query](https://doug-martin.github.io/nestjs-query/docs).
