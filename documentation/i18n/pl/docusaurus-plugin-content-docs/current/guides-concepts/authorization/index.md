---
title: "Authorization | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "Użyj accessControlProvider, aby kontrolować dostęp do zasobów i akcji."
slug: /guides-concepts/authorization
---

Authorization określa, co zalogowany użytkownik może zrobić w aplikacji. W Refine odpowiada za to `accessControlProvider`, który sprawdza uprawnienia dla resource, akcji i opcjonalnych parametrów.

## accessControlProvider

Najważniejszą metodą jest `can`. Otrzymuje ona informacje o akcji, resource i `params`, a zwraca decyzję, czy operacja jest dozwolona.

```tsx title=App.tsx
<Refine
  accessControlProvider={{
    can: async ({ resource, action }) => {
      return { can: resource === "posts" && action === "list" };
    },
  }}
/>
```

## Akcje i zasoby

Typowe akcje to `list`, `create`, `edit`, `show`, `delete` i własne operacje domenowe. Resource pochodzi z konfiguracji `resources`, dlatego dobrze jest utrzymywać spójne nazwy między routingiem, data providerem i authorization.

## Ukrywanie UI

Authorization wpływa nie tylko na dostęp do stron. Może też ukrywać przyciski create, edit i delete, blokować elementy menu albo zmieniać widoczność pól w formularzach. UI powinien jednak traktować to jako wygodę dla użytkownika, a nie jedyną warstwę bezpieczeństwa.

## Integracja z backendem

W aplikacjach produkcyjnych ostateczna decyzja powinna być egzekwowana po stronie API. `accessControlProvider` może korzystać z ról użytkownika, claims w tokenie, odpowiedzi backendu albo zewnętrznych systemów policy, takich jak Casbin, Cerbos czy Permify.

## Dobra praktyka

Trzymaj reguły authorization blisko modelu domeny. Gdy reguły zależą od właściciela rekordu, organizacji albo tenant ID, przekaż potrzebne dane przez `params`, aby decyzja była jawna i testowalna.
