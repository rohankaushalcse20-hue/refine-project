# Integracja kbar dla Refine

`@refinedev/kbar` dodaje paletę komend opartą na [kbar](https://kbar.vercel.app/) do aplikacji Refine. Pomaga użytkownikom szybko przechodzić między resources i wykonywać akcje przez jedno command menu.

## Instalacja

```sh
npm install @refinedev/kbar
```

## Podstawowe użycie

Podłącz provider i komponenty UI z `@refinedev/kbar` wokół aplikacji Refine.

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";
```

Paleta komend dobrze pasuje do interfejsów administracyjnych z dużą liczbą resources, gdzie szybka nawigacja jest ważniejsza niż głęboko zagnieżdżone menu.

## Dokumentacja

- Otwórz [dokumentację command palette](https://refine.dev/docs/packages/command-palette/).
- Więcej o kbar znajdziesz w [dokumentacji kbar](https://kbar.vercel.app/).
