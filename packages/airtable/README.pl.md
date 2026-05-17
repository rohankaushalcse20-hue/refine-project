# Integracja Airtable dla Refine

`@refinedev/airtable` udostępnia data provider do pracy Refine z [Airtable](https://www.airtable.com/). Pozwala używać baz Airtable jako źródła danych dla ekranów CRUD, paneli administracyjnych i narzędzi wewnętrznych.

## Instalacja

```sh
npm install @refinedev/airtable
```

## Podstawowe użycie

Podłącz provider do `Refine` i przekaż parametry dostępu do Airtable. Refine nadal korzysta ze standardowych hooków danych, takich jak `useList`, `useOne`, `useCreate`, `useUpdate` i `useDelete`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/airtable";
```

Pakiet sprawdza się przy szybkich interfejsach administracyjnych nad tabelami Airtable, bez budowania osobnego REST API.

## Dokumentacja

- Otwórz [dokumentację Airtable data provider](https://refine.dev/docs/data/packages/airtable/).
- Ogólne zasady opisuje [dokumentacja data provider](https://refine.dev/docs/data/data-provider/).
