---
title: "Forms | Refine v5"
display_title: "Formularze"
sidebar_label: "Formularze"
description: "Buduj formularze create i edit z hookami Refine oraz wybraną biblioteką UI."
slug: /guides-concepts/forms
---

Formularze w Refine łączą logikę danych z biblioteką UI. Hooki takie jak `useForm` przygotowują zapisywanie, walidację po stronie serwera i przekierowania, a komponenty UI odpowiadają za wygląd pól.

## useForm

`useForm` jest najczęściej używanym hookiem dla stron create i edit. Korzysta z `dataProvider`, aby wykonać `create` albo `update`, oraz z router providera, aby po zapisie przejść do właściwego widoku.

```tsx title=CreatePage.tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "create",
});
```

## Biblioteki UI

Refine dostarcza integracje formularzy dla Ant Design, Material UI, Mantine, Chakra UI i React Hook Form. W trybie headless możesz użyć `@refinedev/core` i podłączyć własne komponenty bez zmiany kontraktu danych.

## Walidacja

Walidacja może działać po stronie klienta, po stronie serwera albo w obu miejscach. Gdy backend zwraca błędy pól, warto mapować je na strukturę oczekiwaną przez wybraną bibliotekę formularzy, aby użytkownik widział komunikat przy konkretnym polu.

## Relacje i selecty

Hooki takie jak `useSelect` pomagają zasilać pola wyboru danymi z innych resources. To typowy przypadek dla formularzy, w których użytkownik wybiera kategorię, właściciela, status albo powiązany rekord.

## Przepływ zapisu

Po udanym zapisie możesz zostać na stronie, przejść do listy, pokazać widok `show` albo kontynuować edycję. Zachowanie zależy od wymagań produktu i może być ustawione w opcjach hooka.
