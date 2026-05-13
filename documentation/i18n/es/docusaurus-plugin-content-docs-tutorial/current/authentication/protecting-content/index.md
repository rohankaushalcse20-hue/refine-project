---
title: Proteger contenido
---

import { Sandpack, CreateAuthProviderFile, AddAuthProviderToAppTsx, AddCheckMethodToAuthProvider, AddAuthenticatedComponentToAppTsx } from "./sandpack.tsx";

<Sandpack>

En este paso implementaremos un `authProvider` básico con el método `check` para validar el estado de autenticación del usuario, lo que nos permitirá proteger nuestro contenido frente a usuarios no autenticados.

Refine puede trabajar con cualquier solución de autenticación gracias a su interfaz `authProvider`, que es fácil de implementar. Configuraremos una implementación para nuestra fake REST API, que también ofrece endpoints de autenticación sencillos.

Para obtener más información sobre los auth providers soportados, consulta la sección [Supported Authentication Providers](/core/docs/guides-concepts/authentication/#supported-auth-providers) de la guía Authentication.

## Crear un Auth Provider

Implementaremos cada método uno por uno, asegurándonos de cubrir todos los detalles.

Primero crearemos un archivo `src/providers/auth-provider.ts` en nuestro proyecto. Este archivo contendrá todos los métodos que debemos implementar para nuestro auth provider.

<CreateAuthProviderFile />

Después pasaremos nuestro auth provider al componente `<Refine />` en el archivo `src/App.tsx` mediante la prop `authProvider`.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

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

## Implementar el método `check`

El método `check` lo usan el hook `useIsAuthenticated` y el componente `<Authenticated />` para comprobar el estado de autenticación del usuario. Debe devolver una `Promise` que se resuelve en un objeto.

Si el usuario está autenticado, el objeto debe contener la propiedad `authenticated: true`. De lo contrario, debe contener la propiedad `authenticated: false`.

Obtendremos un access token mediante el método `login` desde nuestra API y lo guardaremos en local storage. Ahora comprobemos si el token existe en local storage.

Actualiza tu archivo `src/providers/auth-provider.ts` agregando las siguientes líneas:

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

## Usar el componente `<Authenticated />`

Después de implementar el método `check`, podremos usar el componente `<Authenticated />` para proteger nuestro contenido frente a usuarios no autenticados.

Agreguemos el componente `<Authenticated />` a nuestro archivo `src/App.tsx` y envolvamos con él nuestro contenido dentro del componente `<Refine />`.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

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

Observa que agregamos la prop `key` a nuestro componente `<Authenticated />`. Esto es necesario para que el componente funcione correctamente, especialmente cuando se usa varias veces en el mismo árbol de renderizado.

:::

Ahora deberías poder ver el componente `<Authenticated />` en acción. Nuestro contenido no se renderizará y en su lugar se renderizará la prop `fallback`.

:::tip

También puedes usar el hook `useIsAuthenticated`, que el componente `<Authenticated />` usa internamente. Puedes aprender más en la documentación del hook [useIsAuthenticated](/core/docs/authentication/hooks/use-is-authenticated/).

:::

En el siguiente paso implementaremos la funcionalidad de login y logout, y haremos que nuestro método `check` funcione correctamente.

</Sandpack>
