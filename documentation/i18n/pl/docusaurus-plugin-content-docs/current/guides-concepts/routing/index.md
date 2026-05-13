---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Dowiedz się, jak Refine współpracuje z routerami React, Next.js i Remix."
slug: /guides-concepts/routing
---

Refine nie narzuca jednego routera. Zamiast tego używa kontraktu router provider, który łączy `resources` z nawigacją, generowaniem ścieżek i odczytem parametrów URL.

## Rola router providera

Router provider pozwala Refine:

- tworzyć linki do akcji `list`, `create`, `edit`, `show` i `clone`;
- odczytywać parametry, takie jak `id` resource;
- synchronizować filtry, sortowanie i paginację z adresem URL;
- integrować breadcrumbs, menu i przekierowania po mutacjach.

## Resources i ścieżki

Ścieżki podane w `resources` są źródłem prawdy dla nawigacji. Refine używa ich w hookach i komponentach, ale nie zmienia składni routera wybranego przez aplikację.

```tsx title=App.tsx
<Refine
  routerProvider={routerProvider}
  resources={[
    {
      name: "orders",
      list: "/orders",
      show: "/orders/:id",
      edit: "/orders/:id/edit",
    },
  ]}
/>
```

## Wybór integracji

W aplikacjach SPA często używa się React Router. Dla aplikacji renderowanych po stronie serwera można wybrać integracje Next.js albo Remix. Koncepcje Refine pozostają te same: `resources` opisują adresy, a router provider tłumaczy je na mechanizmy danego frameworka.

## Synchronizacja stanu z URL

Listy i tabele mogą przechowywać filtry, sortowanie i paginację w URL. Ułatwia to udostępnianie widoków, powrót do poprzedniego stanu i debugowanie zapytań. Ta funkcja jest szczególnie przydatna w narzędziach wewnętrznych, w których użytkownicy często wracają do zapisanych zestawów filtrów.
