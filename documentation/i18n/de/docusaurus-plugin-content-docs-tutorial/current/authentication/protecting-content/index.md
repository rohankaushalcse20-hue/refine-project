---
title: Inhalte schuetzen
---

import { Sandpack, CreateAuthProviderFile, AddAuthProviderToAppTsx, AddCheckMethodToAuthProvider, AddAuthenticatedComponentToAppTsx } from "./sandpack.tsx";

<Sandpack>

In diesem Schritt implementieren wir einen einfachen `authProvider` mit der Methode `check`, um den Authentifizierungsstatus des Benutzers zu pruefen. Dadurch koennen wir unsere Inhalte vor nicht authentifizierten Benutzern schuetzen.

Refine kann mit jeder Authentifizierungsloesung arbeiten, weil die Schnittstelle `authProvider` einfach zu implementieren ist. Wir richten eine Implementierung fuer unsere Fake-REST-API ein, die auch einfache Authentifizierungs-Endpunkte bereitstellt.

Mehr ueber unterstuetzte Auth Provider findest du im Abschnitt [Supported Authentication Providers](/core/docs/guides-concepts/authentication/#supported-auth-providers) des Authentication-Leitfadens.

## Einen Auth Provider erstellen

Wir implementieren jede Methode einzeln, damit alle Details gruendlich abgedeckt sind.

Zuerst erstellen wir in unserem Projekt die Datei `src/providers/auth-provider.ts`. Sie enthaelt alle Methoden, die wir fuer unseren Auth Provider implementieren muessen.

<CreateAuthProviderFile />

Danach uebergeben wir unseren Auth Provider in der Datei `src/App.tsx` ueber die Prop `authProvider` an die Komponente `<Refine />`.

Aktualisiere deine Datei `src/App.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
// highlight-next-line
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

export default function App(): JSX.Element {
  return (
    <Refine
      dataProvider={dataProvider}
      // highlight-next-line
      authProvider={authProvider}
    >
      {/* <ShowProduct /> */}
      {/* <EditProduct /> */}
      <ListProducts />
      {/* <CreateProduct /> */}
    </Refine>
  );
}
```

<AddAuthProviderToAppTsx />

## Die Methode `check` implementieren

Die Methode `check` wird vom Hook `useIsAuthenticated` und von der Komponente `<Authenticated />` verwendet, um den Authentifizierungsstatus des Benutzers zu pruefen. Sie sollte ein `Promise` zurueckgeben, das zu einem Objekt aufgeloest wird.

Wenn der Benutzer authentifiziert ist, sollte das Objekt die Eigenschaft `authenticated: true` enthalten. Andernfalls sollte es die Eigenschaft `authenticated: false` enthalten.

Wir erhalten ueber die Methode `login` ein Access Token von unserer API und speichern es im Local Storage. Jetzt pruefen wir, ob das Token im Local Storage existiert.

Aktualisiere deine Datei `src/providers/auth-provider.ts`, indem du die folgenden Zeilen hinzufuegst:

```ts title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  // highlight-start
  check: async () => {
    // When logging in, we'll obtain an access token from our API and store it in the local storage.
    // Now let's check if the token exists in the local storage.
    // In the later steps, we'll be implementing the `login` and `logout` methods.
    const token = localStorage.getItem("my_access_token");

    return { authenticated: Boolean(token) };
  },
  // highlight-end
  login: async ({ email, password }) => {
    throw new Error("Not implemented");
  },
  logout: async () => {
    throw new Error("Not implemented");
  },
  onError: async (error) => {
    throw new Error("Not implemented");
  },
  // ...
};
```

<AddCheckMethodToAuthProvider />

## Die Komponente `<Authenticated />` verwenden

Nachdem wir die Methode `check` implementiert haben, koennen wir die Komponente `<Authenticated />` verwenden, um unsere Inhalte vor nicht authentifizierten Benutzern zu schuetzen.

Fuegen wir die Komponente `<Authenticated />` zu unserer Datei `src/App.tsx` hinzu und legen sie um unsere Inhalte innerhalb der Komponente `<Refine />`.

Aktualisiere deine Datei `src/App.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/App.tsx"
// highlight-next-line
import { Refine, Authenticated } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider} authProvider={authProvider}>
      {/* highlight-start */}
      <Authenticated key="protected" fallback={<div>Not authenticated</div>}>
        {/* <ShowProduct /> */}
        {/* <EditProduct /> */}
        <ListProducts />
        {/* <CreateProduct /> */}
      </Authenticated>
      {/* highlight-end */}
    </Refine>
  );
}
```

<AddAuthenticatedComponentToAppTsx />

:::note

Beachte, dass wir der Komponente `<Authenticated />` die Prop `key` hinzugefuegt haben. Das ist erforderlich, damit die Komponente korrekt funktioniert, besonders wenn sie mehrfach im selben Render-Tree verwendet wird.

:::

Jetzt solltest du die Komponente `<Authenticated />` in Aktion sehen. Unsere Inhalte werden nicht gerendert; stattdessen wird die Prop `fallback` angezeigt.

:::tip

Du kannst stattdessen auch den Hook `useIsAuthenticated` verwenden. Die Komponente `<Authenticated />` nutzt diesen Hook intern. Mehr dazu findest du in der Dokumentation zum Hook [useIsAuthenticated](/core/docs/authentication/hooks/use-is-authenticated/).

:::

Im naechsten Schritt implementieren wir die Login- und Logout-Funktionalitaet und sorgen dafuer, dass unsere Methode `check` korrekt arbeitet.

</Sandpack>
