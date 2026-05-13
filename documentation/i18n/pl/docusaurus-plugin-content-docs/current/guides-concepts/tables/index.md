---
title: "Tables | Refine v5"
display_title: "Tabele"
sidebar_label: "Tabele"
description: "Twórz listy i tabele danych z paginacją, sortowaniem i filtrami."
slug: /guides-concepts/tables
---

Tabele są jednym z najczęstszych widoków w aplikacjach CRUD. Refine dostarcza hooki, które łączą `dataProvider` z biblioteką UI i pomagają obsłużyć paginację, sortowanie, filtry oraz synchronizację z URL.

## useTable

`useTable` buduje warstwę danych dla tabeli. Pobiera rekordy przez `dataProvider.getList`, przekazuje parametry paginacji i sortowania, a następnie zwraca właściwości potrzebne wybranej integracji UI.

```tsx title=ListPage.tsx
const { tableProps } = useTable({
  resource: "products",
  syncWithLocation: true,
});
```

## Filtrowanie i sortowanie

Filtry i sortery są przekazywane w przewidywalnym formacie do `dataProvider`. Provider decyduje, jak przetłumaczyć je na parametry REST, zapytanie GraphQL albo składnię konkretnego backendu.

## Synchronizacja z adresem

`syncWithLocation` zapisuje stan tabeli w URL. Dzięki temu użytkownik może udostępnić link do listy z konkretną stroną, filtrem i sortowaniem, a po odświeżeniu wrócić do tego samego widoku.

## Akcje wiersza

Typowe akcje wiersza to `show`, `edit`, `clone` i `delete`. Refine korzysta z konfiguracji `resources`, aby zbudować właściwe ścieżki i sprawdzić uprawnienia przez `accessControlProvider`.

## Wydajność

Dla dużych zbiorów danych filtruj, sortuj i paginuj po stronie serwera. Tabela powinna pokazywać tylko potrzebny wycinek danych, a `dataProvider` powinien zwracać także łączną liczbę rekordów, jeśli UI jej wymaga.
