# Integracja GraphQL dla Refine

`@refinedev/graphql` udostępnia data provider dla GraphQL API. Pakiet pomaga używać standardowych hooków CRUD Refine nad schematami GraphQL bez pisania osobnej warstwy stanu i zapytań dla każdego ekranu.

## Instalacja

```sh
npm install @refinedev/graphql
```

## Podstawowe użycie

Podłącz GraphQL endpoint do providera i przekaż go do `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/graphql";
```

Po konfiguracji możesz używać `useList`, `useOne`, `useCreate`, `useUpdate`, `useDelete` i innych hooków danych Refine w standardowym formacie.

## Dokumentacja

- Otwórz [dokumentację GraphQL data provider](https://refine.dev/docs/data/packages/graphql/).
- Ogólne zasady opisuje [dokumentacja data provider](https://refine.dev/docs/data/data-provider/).
