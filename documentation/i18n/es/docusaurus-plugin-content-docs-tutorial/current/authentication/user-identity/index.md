---
title: Usar la identidad del usuario
---

import { Sandpack, AddGetIdentityMethodToAuthProvider, AddUseGetIdentityToHeaderComponent } from "./sandpack.tsx";

<Sandpack>

En los pasos anteriores agregamos funcionalidades de login y logout, y protegimos nuestro contenido frente a usuarios no autenticados. Ahora aprenderemos a usar el hook `useGetIdentity` de Refine para obtener la identidad del usuario desde nuestra API e implementar el método `getIdentity` en nuestro auth provider.

Implementaremos un componente sencillo llamado `UserGreeting` para mostrar un mensaje de bienvenida al usuario.

## Implementar el método `getIdentity`

El método `getIdentity` se usa para obtener la identidad del usuario desde nuestra API. Debe devolver una `Promise` que se resuelve en un objeto. Ese objeto debe contener la identidad del usuario.

Nuestra fake REST API requiere que enviemos una solicitud `GET` al endpoint `/auth/me` con el `token` en el header `Authorization`. Devolverá la identidad del usuario en el cuerpo de la respuesta.

Actualiza tu archivo `src/providers/auth-provider.ts` agregando las siguientes líneas:

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

## Usar el hook `useGetIdentity`

Después de implementar el método `getIdentity`, podremos llamar al hook `useGetIdentity` y obtener la identidad del usuario desde nuestra API.

Ahora usaremos el hook `useGetIdentity` dentro de nuestro componente `<Header />` para saludar al usuario.

Actualiza tu archivo `src/components/header.tsx` agregando las siguientes líneas:

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

Ahora, cuando iniciemos sesión, deberíamos poder ver un mensaje de bienvenida con el nombre del usuario en pantalla.

:::simple Note

Para fines de demostración, nuestra fake REST API devuelve "John Doe" como nombre de usuario, independientemente del token enviado.

:::

En este punto ya configuramos el flujo básico de autenticación. En el siguiente paso aprenderemos a integrarlo con nuestro data provider.

</Sandpack>
