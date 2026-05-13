---
title: Redirecciones
---

import { Sandpack, AddRedirectsToAuthProvider, AddCustomRedirectToCreate, AddCustomRedirectToEdit } from "./sandpack.tsx";

<Sandpack>

Ahora actualizamos nuestros componentes para aprovechar la inferencia de parámetros de Refine. En este paso aprenderemos sobre las redirecciones y cómo aprovecharlas en nuestros formularios y auth provider.

Refine puede gestionar redirecciones automáticamente por ti. Después de enviar un formulario correctamente, Refine intentará redirigir al usuario a la página apropiada.

Al igual que los formularios, las redirecciones también están soportadas en el auth provider. Al proporcionar un parámetro `redirectTo` en los valores de retorno de los métodos `login`, `logout` y `onError`, puedes redirigir al usuario a la página apropiada, como la página índice después de un login correcto o la página de login después de un logout correcto.

## Redirigir después de enviar un formulario

Por defecto, Refine redirigirá al usuario a la página de lista del resource objetivo después de enviar un formulario correctamente. Podemos personalizar este comportamiento proporcionando un parámetro `redirect` al hook `useForm`.

:::tip

También puedes usar la prop `options.redirect` del componente `<Refine />` para establecer una redirección predeterminada para todos los formularios por acción.

:::

### Mostrar el registro después de actualizarlo

Actualicemos nuestro componente `<EditProduct />` y proporcionemos un parámetro `redirect` para redirigir a los usuarios a la página show del producto editado después de enviar el formulario correctamente.

Actualiza tu archivo `src/pages/products/edit.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/edit.tsx"
import { useForm, useSelect } from "@refinedev/core";

export const EditProduct = () => {
  const { onFinish, mutation, query } = useForm({
    // highlight-start
    // This will redirect to the show page after the mutation is successful.
    // Default value is `"list"`.
    // We can also provide `false` to disable the redirect.
    redirect: "show",
    // highlight-end
  });

  /* ... */
};
```

<AddCustomRedirectToEdit />

### Continuar editando el registro después de crearlo

Actualicemos nuestro componente `<CreateProduct />` y proporcionemos un parámetro `redirect` para permitir que los usuarios sigan editando el producto creado después de enviar el formulario correctamente.

Actualiza tu archivo `src/pages/products/create.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/create.tsx"
import { useForm, useSelect } from "@refinedev/core";

export const CreateProduct = () => {
  const { onFinish, mutation } = useForm({
    // highlight-start
    // We can also provide `false` to disable the redirect.
    // Default value is `"list"`.
    redirect: "edit",
    // highlight-end
  });

  /* ... */
};
```

<AddCustomRedirectToCreate />

## Gestionar redirecciones en Auth Provider

Refine proporciona una forma sencilla de integrar routing en tu auth provider. Al proporcionar un parámetro `redirectTo` en los valores de retorno de los métodos `login`, `logout` y `onError`, puedes redirigir al usuario a la página apropiada, como la página índice después de un login correcto o la página de login después de un logout correcto.

Actualicemos nuestro archivo `src/providers/auth-provider.ts` y proporcionemos propiedades `redirectTo` en los valores de retorno de los métodos `login` y `logout`. Queremos redirigir al usuario a la página índice después de un login correcto y a la página de login después de un logout correcto.

Actualiza tu archivo `src/providers/auth-provider.ts` agregando las siguientes líneas:

```tsx title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  logout: async () => {
    localStorage.removeItem("my_access_token");

    // highlight-start
    // Let's redirect to the login page after a successful logout.
    return { success: true, redirectTo: "/login" };
    // highlight-end
  },
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
      // highlight-start
      // Let's redirect to the index page after a successful login.
      return { success: true, redirectTo: "/" };
      // highlight-end
    }

    return { success: false };
  },
  /* ... */
};
```

<AddRedirectsToAuthProvider />

Ahora aprendimos sobre las redirecciones y cómo aprovecharlas en formularios y auth provider. Continuemos con el siguiente paso, donde aprenderemos a guardar el estado `currentPage` de la tabla en la URL.

</Sandpack>
