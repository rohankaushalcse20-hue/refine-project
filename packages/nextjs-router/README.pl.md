# Next.js router provider dla Refine

`@refinedev/nextjs-router` podłącza Refine do routingu Next.js. Pakiet udostępnia router provider, który pomaga resources Refine synchronizować się z URL, nawigacją i stronami aplikacji Next.js.

## Instalacja

```sh
npm install @refinedev/nextjs-router
```

## Podstawowe użycie

Zaimportuj router provider i przekaż go do `Refine` razem z pozostałymi providerami aplikacji.

```tsx
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/nextjs-router";
```

Integracja jest przydatna w projektach, w których ekrany Refine mają działać wewnątrz Next.js oraz korzystać z jego modelu stron, layoutów i nawigacji.

## Dokumentacja

- Przeczytaj [dokumentację router provider](https://refine.dev/docs/core/providers/router-provider/).
- Przykłady Next.js znajdziesz w [sekcji examples](https://refine.dev/docs/examples/next-js/next-js/).
