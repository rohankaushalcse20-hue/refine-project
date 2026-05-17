# React Router provider dla Refine

`@refinedev/react-router` podłącza Refine do [React Router](https://reactrouter.com/). Pakiet udostępnia router provider, który synchronizuje resources Refine z URL, nawigacją i zagnieżdżonymi trasami aplikacji React.

## Instalacja

```sh
npm install @refinedev/react-router react-router
```

## Podstawowe użycie

Przekaż `routerProvider` do `Refine` i zdefiniuj trasy aplikacji przez React Router.

```tsx
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
```

Integracja pomaga używać hooków nawigacyjnych Refine, breadcrumbs, menu i resource-based routing bez ręcznego łączenia każdej trasy.

## Dokumentacja

- Przeczytaj [dokumentację router provider](https://refine.dev/docs/core/providers/router-provider/).
- Przykład znajdziesz w [React Router example](https://refine.dev/docs/examples/react-router/).
