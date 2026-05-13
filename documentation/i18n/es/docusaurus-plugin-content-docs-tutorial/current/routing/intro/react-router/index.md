---
title: Introducción
---

import { Sandpack, AddRouterProviderToApp } from "./sandpack.tsx";

<Sandpack>

Ahora ya aprendimos los fundamentos de data fetching y los conceptos básicos de autenticación en Refine. En esta unidad aprenderemos a agregar un router provider a nuestra app y las funcionalidades que habilita.

Refine ofrece integraciones para las opciones de routing más populares, como [React Router](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) y [Remix](/core/docs/routing/integrations/remix).

:::simple Consejos de implementación

- Se recomienda elegir una integración integrada para tu router, pero si quieres usar una solución personalizada puedes crear tu propio provider con la [interfaz de router provider](/core/docs/routing/router-provider) de Refine, que es fácil de usar.

- Refine no interferirá con la forma en que tu router gestiona la navegación. Generarás las rutas o páginas como normalmente lo harías con tu router.

- Proporcionar un router provider a Refine habilitará muchas funcionalidades sin renunciar a ninguna de las capacidades de tu router.

:::

Esta unidad cubrirá los siguientes temas:

- El concepto de resource en Refine y cómo usarlo,
- Usar la integración de router para inferir parámetros como `resource`, `action` e `id` desde la URL,
- Gestionar navegación y redirecciones en Refine,
- Usar la integración de router para guardar estados de formularios y tablas en la URL,
- Finalmente, gestionar la autenticación con opciones de router.

Esta unidad será agnóstica al framework UI. Las partes de routing relacionadas con los frameworks UI se cubrirán en las siguientes unidades.

## Agregar Router Provider

Comencemos agregando nuestras dependencias. Para routing usaremos `react-router` y, para integrarlo con Refine, usaremos el paquete `@refinedev/react-router`.

<InstallPackagesCommand args="react-router @refinedev/react-router"/>

Después pasaremos nuestro router provider al componente `<Refine />`. Además, envolveremos nuestra app con `<BrowserRouter />` de `react-router`.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";
// highlight-next-line
import routerProvider from "@refinedev/react-router";

// highlight-next-line
import { BrowserRouter } from "react-router";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

import { Login } from "./pages/login";
import { Header } from "./components/header";

export default function App(): JSX.Element {
  return (
    // highlight-next-line
    <BrowserRouter>
      <Refine
        dataProvider={dataProvider}
        authProvider={authProvider}
        // highlight-next-line
        routerProvider={routerProvider}
      >
        <Authenticated key="protected" fallback={<Login />}>
          <Header />
          {/* <ShowProduct /> */}
          {/* <EditProduct /> */}
          <ListProducts />
          {/* <CreateProduct /> */}
        </Authenticated>
      </Refine>
      {/* highlight-next-line */}
    </BrowserRouter>
  );
}
```

<AddRouterProviderToApp />

Ahora estamos listos para empezar a explorar las funcionalidades de la integración de router de Refine.

En el siguiente paso aprenderemos cómo informar a Refine sobre las rutas relacionadas por cada resource.

</Sandpack>
