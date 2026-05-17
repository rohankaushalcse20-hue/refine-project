# Integracja Appwrite dla Refine

`@refinedev/appwrite` udostępnia data provider dla [Appwrite](https://appwrite.io/). Łączy standardowe hooki CRUD Refine z kolekcjami Appwrite i pomaga budować narzędzia wewnętrzne nad istniejącym projektem backendowym.

## Instalacja

```sh
npm install @refinedev/appwrite
```

## Podstawowe użycie

Zaimportuj `dataProvider` z `@refinedev/appwrite`, skonfiguruj klienta Appwrite i przekaż provider do `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import { dataProvider } from "@refinedev/appwrite";
```

Po podłączeniu możesz używać `useList`, `useOne`, `useCreate`, `useUpdate` i innych hooków danych bez osobnej warstwy zapytań w interfejsie.

## Dokumentacja

- Otwórz [dokumentację Appwrite data provider](https://refine.dev/docs/data/packages/appwrite/).
- Referencję Appwrite znajdziesz w [oficjalnej dokumentacji](https://appwrite.io/docs).
