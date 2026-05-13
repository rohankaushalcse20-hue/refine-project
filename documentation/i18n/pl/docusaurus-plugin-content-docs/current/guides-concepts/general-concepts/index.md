---
title: "General Concepts | Refine v5"
display_title: "Koncepcje ogólne"
sidebar_label: "Koncepcje ogólne"
description: "Poznaj podstawowe elementy architektury Refine: resources, providers, hooks i mutation modes."
slug: /guides-concepts/general-concepts
---

Refine organizuje aplikację wokół kilku stabilnych kontraktów. Najważniejsze z nich to `resources`, providery i hooki, które pozwalają opisać logikę CRUD bez wiązania jej z konkretną biblioteką UI.

## Resources

`resources` opisują encje domeny aplikacji. Każdy resource może mieć ścieżki `list`, `create`, `edit`, `show` i `clone`, a także metadane używane przez menu, breadcrumbs i uprawnienia.

```tsx title=App.tsx
<Refine
  resources={[
    {
      name: "products",
      list: "/products",
      create: "/products/new",
      edit: "/products/:id/edit",
      show: "/products/:id",
      meta: {
        canDelete: true,
      },
    },
  ]}
/>
```

## Providers

Providery są granicą między Refine a zewnętrznymi usługami. `dataProvider` komunikuje się z API, `authProvider` obsługuje authentication, `accessControlProvider` odpowiada za authorization, a `notificationProvider` pokazuje komunikaty dla użytkownika.

## Hooks

Hooki Refine, takie jak `useList`, `useOne`, `useCreate`, `useUpdate`, `useTable` i `useForm`, korzystają z providerów i resources. Dzięki temu logika danych pozostaje taka sama, niezależnie od tego, czy UI powstaje w Material UI, Ant Design, Mantine, Chakra UI czy w komponentach własnych.

## Mutation modes

Refine wspiera różne tryby mutacji. `pessimistic` czeka na odpowiedź serwera, `optimistic` aktualizuje UI natychmiast, a `undoable` daje użytkownikowi krótkie okno na cofnięcie operacji. Wybór trybu zależy od ryzyka danych i oczekiwanego doświadczenia użytkownika.

## Co dalej?

Po zrozumieniu tych elementów przejdź do [Routing](/core/docs/guides-concepts/routing/) i [Data Fetching](/core/docs/guides-concepts/data-fetching/), gdzie te same kontrakty są pokazane w praktyce.
