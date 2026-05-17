# Integracja Hasura dla Refine

`@refinedev/hasura` podłącza Refine do [Hasura](https://hasura.io/) przez GraphQL API. Pakiet pomaga szybko budować interfejsy CRUD nad danymi, które Hasura publikuje z uwzględnieniem schematu i reguł dostępu.

## Instalacja

```sh
npm install @refinedev/hasura
```

## Podstawowe użycie

Zaimportuj `dataProvider` z `@refinedev/hasura`, skonfiguruj endpoint Hasura i przekaż provider do `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/hasura";
```

Integracja pasuje do aplikacji, w których backend jest już opisany w Hasura, a interfejs potrzebuje list, formularzy i stron podglądu opartych na resources Refine.

## Dokumentacja

- Przeczytaj [dokumentację Hasura data provider](https://refine.dev/docs/data/packages/hasura/).
- Oficjalne materiały znajdziesz w [dokumentacji Hasura](https://hasura.io/docs/).
