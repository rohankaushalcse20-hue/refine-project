# Refine Devtools

`@refinedev/devtools` dodaje narzędzia deweloperskie dla aplikacji Refine. Devtools pomagają debugować zapytania i mutacje, sprawdzać wygenerowany kod Inferencer, przeglądać ustawienia projektu i szybciej znajdować problemy podczas developmentu.

## Instalacja

Najpierw upewnij się, że masz aktualny `@refinedev/cli`.

```sh
npm install @refinedev/cli@latest
```

Następnie zainicjalizuj devtools w projekcie.

```sh
npm run refine devtools init
```

## Użycie

Devtools działają tylko w development mode i nie dodają narzutu do produkcyjnego buildu. Można je pozostawić podłączone w projekcie bez dodatkowych kroków wykluczania z production bundle.

## Dokumentacja

- Przeczytaj [dokumentację Devtools](https://refine.dev/docs/guides-concepts/development/#refine-devtools).
- Jeśli CLI nie jest jeszcze podłączone, otwórz [instrukcję instalacji CLI](https://refine.dev/docs/packages/cli/#how-to-add-to-an-existing-project).
