---
title: "Authentication | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "Skonfiguruj authProvider, aby obsługiwać logowanie, wylogowanie i sprawdzanie sesji w Refine."
slug: /guides-concepts/authentication
---

Authentication w Refine jest obsługiwane przez `authProvider`. Dzięki temu aplikacja może używać dowolnego mechanizmu tożsamości: własnego API, Auth0, Keycloak, Google, Azure AD albo innego dostawcy.

## Zadania authProvider

`authProvider` zwykle implementuje metody:

- `login` do rozpoczęcia sesji użytkownika;
- `logout` do zakończenia sesji;
- `check` do sprawdzania, czy użytkownik nadal jest zalogowany;
- `getIdentity` do pobrania danych profilu;
- `onError` do reakcji na błędy API, na przykład wygaśnięty token.

## Ochrona tras

Połączenie `authProvider` z router providerem pozwala zabezpieczać strony create, edit, show i list. Gdy `check` zwróci brak dostępu, aplikacja może przekierować użytkownika na stronę logowania.

```tsx title=App.tsx
<Refine
  authProvider={authProvider}
  resources={[
    {
      name: "posts",
      list: "/posts",
    },
  ]}
/>
```

## Tokeny i sesje

Refine nie narzuca miejsca przechowywania tokenów. Możesz użyć cookies, storage przeglądarki albo sesji po stronie serwera. Ważne, aby `dataProvider` i `authProvider` korzystały z tego samego źródła informacji o aktualnej sesji.

## Doświadczenie użytkownika

Dobre authentication powinno jasno obsługiwać stany ładowania, wygasłe sesje i błędy logowania. `notificationProvider` może pokazywać komunikaty, a `getIdentity` może zasilać UI nazwą, adresem e-mail albo rolą użytkownika.
