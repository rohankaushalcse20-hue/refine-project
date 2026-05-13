---
title: "Quickstart | Refine v5"
display_title: "Quickstart"
sidebar_label: "Quickstart"
description: "Utwórz pierwszą aplikację Refine i uruchom ją lokalnie."
displayed_sidebar: mainSidebar
slug: /getting-started/quickstart
---

Ten quickstart prowadzi przez utworzenie nowej aplikacji Refine, wybór integracji UI oraz uruchomienie serwera developerskiego. Komendy i nazwy pakietów pozostają takie same jak w dokumentacji angielskiej.

## Utwórz projekt

Najprostszą ścieżką jest użycie `create refine-app`:

```sh
npm create refine-app@latest
```

Kreator zapyta o framework, bibliotekę UI, data provider i opcjonalne funkcje. Dla pierwszej aplikacji możesz wybrać konfigurację z Vite, React i `@refinedev/simple-rest`, a później wymienić providery na własne integracje.

## Uruchom aplikację

Po utworzeniu projektu przejdź do katalogu aplikacji i uruchom dev server:

```sh
npm run dev
```

Refine wyrenderuje aplikację z komponentem `<Refine />`, zasobami i providerami skonfigurowanymi przez szablon. W zależności od wybranej biblioteki UI zobaczysz gotowe strony list, create, edit i show.

## Co warto sprawdzić

- Plik `src/App.tsx`, w którym skonfigurowane są `resources` i providery.
- Wybrany `dataProvider`, który mapuje zapytania Refine na API.
- Strony zasobów, które korzystają z hooków takich jak `useTable`, `useForm`, `useList` i `useOne`.
- Konfigurację routingu, jeśli projekt używa React Router, Next.js albo Remix.

## Następne kroki

Gdy aplikacja działa lokalnie, przejdź do [General Concepts](/core/docs/guides-concepts/general-concepts/), aby poznać model `resources`, a potem do [Data Fetching](/core/docs/guides-concepts/data-fetching/), aby zrozumieć kontrakt `dataProvider`.
