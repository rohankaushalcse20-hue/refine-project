---
title: "Data Fetching | Refine v5"
display_title: "Pobieranie danych"
sidebar_label: "Pobieranie danych"
description: "Zobacz, jak Refine używa data providerów i hooków do pracy z API."
slug: /guides-concepts/data-fetching
---

Pobieranie danych w Refine opiera się na kontrakcie `dataProvider`. Ten kontrakt oddziela logikę aplikacji od konkretnego API, dzięki czemu te same hooki mogą działać z REST, GraphQL, Supabase, Strapi, Hasura albo własnym backendem.

## Data provider

`dataProvider` implementuje metody takie jak `getList`, `getOne`, `create`, `update`, `deleteOne`, `getMany` i `custom`. Refine wywołuje je na podstawie resource, akcji i parametrów przekazanych do hooków.

```tsx title=App.tsx
import dataProvider from "@refinedev/simple-rest";

<Refine dataProvider={dataProvider("https://api.fake-rest.refine.dev")} />;
```

## Hooki danych

Najczęściej używane hooki to:

- `useList` do pobierania kolekcji;
- `useOne` do pobierania pojedynczego rekordu;
- `useCreate`, `useUpdate` i `useDelete` do mutacji;
- `useTable` do połączenia listy z paginacją, sortowaniem i filtrowaniem;
- `useForm` do obsługi formularzy create i edit.

## Parametry zapytań

Hooki przekazują do `dataProvider` informacje o paginacji, sortowaniu, filtrach i `meta`. Dzięki temu provider może zbudować odpowiednie zapytanie HTTP albo GraphQL bez zmiany komponentów UI.

## Obsługa błędów

Błędy zwracane przez `dataProvider` trafiają do hooków i mogą zostać pokazane przez `notificationProvider`. W aplikacjach produkcyjnych warto normalizować błędy backendu tak, aby komponenty otrzymywały przewidywalny format.

## Wiele źródeł danych

Refine może używać wielu data providerów w jednej aplikacji. To przydatne, gdy panel administracyjny łączy własne API, usługę wyszukiwania i zewnętrzny system billingowy.
