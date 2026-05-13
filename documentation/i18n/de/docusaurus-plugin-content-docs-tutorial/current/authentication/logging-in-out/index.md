---
title: An- und Abmelden
---

import { Sandpack, AddLoginMethodToAuthProvider, CreateLoginComponentFile, AddLoginToAppTsx, AddUseLoginToLoginComponent, AddLogoutMethodToAuthProvider, CreateHeaderComponentFile, AddHeaderToAppTsx, AddUseLogoutToHeaderComponent } from "./sandpack.tsx";

<Sandpack>

Im vorherigen Schritt haben wir die Komponente `<Authenticated />` zu unserer Datei `src/App.tsx` hinzugefuegt, um unsere Inhalte vor nicht authentifizierten Benutzern zu schuetzen. Jetzt implementieren wir die Methoden `login` und `logout` in unserem Auth Provider, damit sich Benutzer anmelden und abmelden koennen.

## Die Methode `login` implementieren

Die Methode `login` wird verwendet, um den Benutzer zu authentifizieren und zugehoerige Aufgaben auszufuehren, zum Beispiel das Speichern des Tokens. Sie sollte ein `Promise` zurueckgeben, das zu einem Objekt aufgeloest wird. Das Objekt sollte die Eigenschaft `success` enthalten, die angibt, ob der Login erfolgreich war.

Unsere Fake-REST-API erwartet einen `POST`-Request an den Endpoint `/auth/login` mit den Parametern `email` und `password` im Request Body. Sie gibt im Response Body ein `token` zurueck.

Wir speichern das `token` ausserdem im `localStorage`, damit wir es spaeter verwenden koennen.

Aktualisiere deine Datei `src/providers/auth-provider.ts`, indem du die folgenden Zeilen hinzufuegst:

```ts title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  // highlight-start
  // login method receives an object with all the values you've provided to the useLogin hook.
  login: async ({ email, password }) => {
    const response = await fetch(
      "https://api.fake-rest.refine.dev/auth/login",
      {
        method: "POST",
        body: JSON.stringify({ email, password }),
        headers: {
          "Content-Type": "application/json",
        },
      },
    );

    const data = await response.json();

    if (data.token) {
      localStorage.setItem("my_access_token", data.token);
      return { success: true };
    }

    return { success: false };
  },
  // highlight-end
  check: async () => {
    const token = localStorage.getItem("my_access_token");

    return { authenticated: Boolean(token) };
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

<AddLoginMethodToAuthProvider />

## Den Hook `useLogin` verwenden

Nachdem wir die Methode `login` implementiert haben, koennen wir den Hook `useLogin` aufrufen und Benutzer anmelden. Erstellen wir eine Komponente namens `Login` und mounten sie innerhalb unserer Komponente `<Refine />`.

<CreateLoginComponentFile />

Danach mounten wir unsere Komponente `<Login />` und uebergeben sie in der Datei `src/App.tsx` als Prop `fallback` an die Komponente `<Authenticated />`.

Aktualisiere deine Datei `src/App.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

// highlight-next-line
import { Login } from "./pages/login";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider} authProvider={authProvider}>
      <Authenticated
        key="protected"
        // highlight-next-line
        fallback={<Login />}
      >
        {/* <ShowProduct /> */}
        {/* <EditProduct /> */}
        <ListProducts />
        {/* <CreateProduct /> */}
      </Authenticated>
    </Refine>
  );
}
```

<AddLoginToAppTsx />

Zum Schluss importieren wir den Hook `useLogin` und verwenden ihn in unserer Komponente `Login`, um Benutzer anzumelden.

Aktualisiere deine Datei `src/pages/login.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/pages/login.tsx"
import React from "react";
// highlight-next-line
import { useLogin } from "@refinedev/core";

export const Login = () => {
  // highlight-next-line
  const {
    mutate,
    mutation: { isPending },
  } = useLogin();

  const onSubmit = (event: React.FormEvent<HTMLFormElement>) => {
    event.preventDefault();
    // Using FormData to get the form values and convert it to an object.
    const data = Object.fromEntries(new FormData(event.target).entries());
    // Calling mutate to submit with the data we've collected from the form.
    // highlight-next-line
    mutate(data);
  };

  return (
    <div>
      <h1>Login</h1>
      <form onSubmit={onSubmit}>
        <label htmlFor="email">Email</label>
        <input
          type="email"
          id="email"
          name="email"
          // We're providing default values for demo purposes.
          defaultValue="demo@demo.com"
        />

        <label htmlFor="password">Password</label>
        <input
          type="password"
          id="password"
          name="password"
          // We're providing default values for demo purposes.
          defaultValue="demodemo"
        />

        {isPending && <span>loading...</span>}
        <button type="submit" disabled={isPending}>
          Submit
        </button>
      </form>
    </div>
  );
};
```

<AddUseLoginToLoginComponent />

## Die Methode `logout` implementieren

Die Methode `logout` wird verwendet, um den Benutzer abzumelden und zugehoerige Aufgaben auszufuehren, zum Beispiel das Entfernen des Tokens. Sie sollte ein `Promise` zurueckgeben, das zu einem Objekt aufgeloest wird. Das Objekt sollte die Eigenschaft `success` enthalten, die angibt, ob der Logout erfolgreich war.

Unsere Fake-REST-API erwartet keinen Request, um den Benutzer abzumelden. Wir entfernen einfach das `token` aus dem `localStorage`.

Aktualisiere deine Datei `src/providers/auth-provider.ts`, indem du die folgenden Zeilen hinzufuegst:

```ts title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  // highlight-start
  logout: async () => {
    localStorage.removeItem("my_access_token");
    // We're returning success: true to indicate that the logout operation was successful.
    return { success: true };
  },
  // highlight-end
  // login method receives an object with all the values you've provided to the useLogin hook.
  login: async ({ email, password }) => {
    const response = await fetch(
      "https://api.fake-rest.refine.dev/auth/login",
      {
        method: "POST",
        body: JSON.stringify({ email, password }),
        headers: {
          "Content-Type": "application/json",
        },
      },
    );

    const data = await response.json();

    if (data.token) {
      localStorage.setItem("my_access_token", data.token);
      return { success: true };
    }

    return { success: false };
  },
  check: async () => {
    const token = localStorage.getItem("my_access_token");

    return { authenticated: Boolean(token) };
  },
  onError: async (error) => {
    throw new Error("Not implemented");
  },
  // ...
};
```

<AddLogoutMethodToAuthProvider />

## Den Hook `useLogout` verwenden

Nachdem wir die Methode `logout` implementiert haben, koennen wir den Hook `useLogout` aufrufen und Benutzer abmelden. Erstellen wir eine Komponente namens `Header`, fuegen dort eine Logout-Schaltflaeche hinzu und mounten sie innerhalb unserer Komponente `<Refine />`.

<CreateHeaderComponentFile />

Danach mounten wir unsere Komponente `<Header />` und uebergeben sie in der Datei `src/App.tsx` als Children an die Komponente `<Authenticated />`.

Aktualisiere deine Datei `src/App.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

import { Login } from "./pages/login";
// highlight-next-line
import { Header } from "./components/header";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider} authProvider={authProvider}>
      <Authenticated key="protected" fallback={<Login />}>
        {/* highlight-next-line */}
        <Header />
        {/* <ShowProduct /> */}
        {/* <EditProduct /> */}
        <ListProducts />
        {/* <CreateProduct /> */}
      </Authenticated>
    </Refine>
  );
}
```

<AddHeaderToAppTsx />

Zum Schluss importieren wir den Hook `useLogout` und verwenden ihn in unserer Komponente `Header`, um Benutzer abzumelden.

Aktualisiere deine Datei `src/components/header.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/components/header.tsx"
import React from "react";
// highlight-next-line
import { useLogout } from "@refinedev/core";

export const Header = () => {
  // highlight-next-line
  const {
    mutate,
    mutation: { isPending },
  } = useLogout();

  return (
    <>
      <h2>Welcome!</h2>
      <button
        type="button"
        disabled={isPending}
        // highlight-next-line
        onClick={mutate}
      >
        Logout
      </button>
    </>
  );
};
```

<AddUseLogoutToHeaderComponent />

Jetzt koennen Benutzer sich anmelden und abmelden.

Beachte, dass die Komponente `<Authenticated />` nach dem Anmelden unsere Inhalte statt der Prop `fallback` rendert. Dasselbe gilt beim Abmelden. Refine uebernimmt die Invalidierung der Methode `check` fuer uns, sodass wir uns darum nicht kuemmern muessen.

Im naechsten Schritt lernst du die Benutzeridentitaet kennen und wie du sie in deiner Anwendung verwendest.

</Sandpack>
