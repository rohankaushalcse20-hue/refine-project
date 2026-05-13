---
title: Benutzeridentitaet verwenden
---

import { Sandpack, AddGetIdentityMethodToAuthProvider, AddUseGetIdentityToHeaderComponent } from "./sandpack.tsx";

<Sandpack>

In den vorherigen Schritten haben wir Login- und Logout-Funktionen hinzugefuegt und unsere Inhalte vor nicht authentifizierten Benutzern geschuetzt. Jetzt lernst du Refines Hook `useGetIdentity` kennen, um die Identitaet des Benutzers aus unserer API abzurufen und die Methode `getIdentity` in unserem Auth Provider zu implementieren.

Wir implementieren eine einfache Komponente namens `UserGreeting`, um dem Benutzer eine Willkommensnachricht anzuzeigen.

## Die Methode `getIdentity` implementieren

Die Methode `getIdentity` wird verwendet, um die Identitaet des Benutzers aus unserer API abzurufen. Sie sollte ein `Promise` zurueckgeben, das zu einem Objekt aufgeloest wird. Das Objekt sollte die Identitaet des Benutzers enthalten.

Unsere Fake-REST-API erwartet einen `GET`-Request an den Endpoint `/auth/me` mit dem `token` im Header `Authorization`. Sie gibt die Benutzeridentitaet im Response Body zurueck.

Aktualisiere deine Datei `src/providers/auth-provider.ts`, indem du die folgenden Zeilen hinzufuegst:

```ts title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  // highlight-start
  getIdentity: async () => {
    const response = await fetch("https://api.fake-rest.refine.dev/auth/me", {
      headers: {
        Authorization: localStorage.getItem("my_access_token"),
      },
    });

    if (response.status < 200 || response.status > 299) {
      return null;
    }

    const data = await response.json();

    return data;
  },
  // highlight-end
  logout: async () => {
    /* ... */
  },
  login: async ({ email, password }) => {
    /* ... */
  },
  check: async () => {
    /* ... */
  },
  onError: async (error) => {
    /* ... */
  },
  // ...
};
```

<AddGetIdentityMethodToAuthProvider />

## Den Hook `useGetIdentity` verwenden

Nachdem wir die Methode `getIdentity` implementiert haben, koennen wir den Hook `useGetIdentity` aufrufen und die Identitaet des Benutzers aus unserer API abrufen.

Jetzt verwenden wir den Hook `useGetIdentity` in unserer Komponente `<Header />`, um den Benutzer zu begruessen.

Aktualisiere deine Datei `src/components/header.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/components/header.tsx"
import React from "react";
import { useLogout, useGetIdentity } from "@refinedev/core";

export const Header = () => {
  const { mutate, isPending } = useLogout();
  const { data: identity } = useGetIdentity();

  return (
    <>
      <h2>
        <span>Welcome, </span>
        <span>{identity?.name ?? ""}</span>
      </h2>
      <button type="button" disabled={isPending} onClick={mutate}>
        Logout
      </button>
    </>
  );
};
```

<AddUseGetIdentityToHeaderComponent />

Wenn wir uns jetzt anmelden, sollten wir eine Willkommensnachricht mit dem Namen des Benutzers auf dem Bildschirm sehen.

:::simple Note

Zu Demonstrationszwecken gibt unsere Fake-REST-API unabhaengig vom gesendeten Token den Namen "John Doe" zurueck.

:::

An diesem Punkt haben wir den grundlegenden Authentifizierungsablauf eingerichtet. Im naechsten Schritt lernst du, wie du ihn mit unserem Data Provider integrierst.

</Sandpack>
