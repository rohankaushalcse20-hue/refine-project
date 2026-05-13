---
title: "Notifications | Refine v5"
display_title: "Powiadomienia"
sidebar_label: "Powiadomienia"
description: "Skonfiguruj notificationProvider, aby pokazywać użytkownikom status operacji."
slug: /guides-concepts/notifications
---

Powiadomienia pomagają użytkownikowi zrozumieć wynik operacji: zapis się powiódł, żądanie zakończyło się błędem albo mutację można jeszcze cofnąć. W Refine odpowiada za to `notificationProvider`.

## notificationProvider

Provider udostępnia metody do otwierania i zamykania komunikatów. Integracje UI, takie jak Ant Design, Material UI, Mantine i Chakra UI, mogą podłączyć własny system toastów, alertów albo snackbarów.

```tsx title=App.tsx
<Refine notificationProvider={notificationProvider} />;
```

## Automatyczne komunikaty

Hooki danych mogą wyświetlać powiadomienia po sukcesie albo błędzie. Dzięki temu create, update i delete informują użytkownika bez powtarzania tej samej logiki w każdej stronie.

## Dostosowanie treści

Treść powiadomień można dostosować w opcjach hooków. Warto pisać komunikaty językiem produktu, na przykład "Produkt zapisany" zamiast technicznego "Mutation succeeded".

## Błędy i undoable

Dla mutacji `undoable` powiadomienie pełni dodatkową rolę: daje użytkownikowi możliwość cofnięcia akcji przed wysłaniem trwałej zmiany. Dla błędów API komunikat powinien wskazywać, czy użytkownik może spróbować ponownie, poprawić dane, czy skontaktować się z administratorem.

## Lokalizacja

W aplikacjach wielojęzycznych powiadomienia powinny korzystać z tego samego źródła tłumaczeń co reszta UI. `i18nProvider` może dostarczać teksty, a `notificationProvider` odpowiada za sposób ich pokazania.
