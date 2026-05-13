# @refinedev/core

`@refinedev/core` zawiera headless fundament Refine. Pakiet dostarcza komponent `<Refine />`, kontrakty providerów, hooki danych, obsługę resources, mutation modes oraz integracje potrzebne do budowania aplikacji CRUD niezależnie od biblioteki UI.

## Co obejmuje pakiet?

- Konfigurację `resources` dla akcji `list`, `create`, `edit`, `show` i `clone`.
- Hooki danych, takie jak `useList`, `useOne`, `useCreate`, `useUpdate` i `useDelete`.
- Kontrakty `dataProvider`, `authProvider`, `accessControlProvider`, `notificationProvider`, `i18nProvider` i router provider.
- Mechanizmy state, cache i mutacji używane przez integracje UI Refine.

## Kiedy używać?

Użyj `@refinedev/core`, gdy chcesz kontrolować własną warstwę UI albo zbudować integrację z wybraną biblioteką komponentów. Nazwy API, importy i komendy instalacji pozostają bez tłumaczenia.
