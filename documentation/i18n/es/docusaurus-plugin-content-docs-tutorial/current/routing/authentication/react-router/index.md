---
title: Autenticación
---

import { Sandpack, AddAuthenticationToApp } from "./sandpack.tsx";

<Sandpack>

Antes de empezar a agregar nuestros resources y sus rutas correspondientes, moveremos la lógica de autenticación para que funcione con routing. Para lograrlo, usaremos los componentes `<Authenticated />` y `<NavigateToResource />` para redirigir a los usuarios a nuestra página de lista de productos.

## `<Authenticated />` y routing

En la unidad anterior implementamos nuestro sistema de autenticación y protegimos el contenido frente a usuarios no autenticados usando el componente `<Authenticated />`.

Usamos las props `children` y `fallback` del componente `<Authenticated />` para renderizar nuestro contenido o el componente fallback según el estado de autenticación.

Ahora aprovecharemos estas props para decidir qué rutas renderizar según el estado de autenticación y gestionar las redirecciones para los casos opuestos.

El componente `<Authenticated />` funciona sin problemas con el router provider cuando omitimos la prop `fallback` y usamos la prop `redirectOnFail`. En este caso, redirigirá al usuario a la página de login si no está autenticado.

```tsx
import { Authenticated } from "@refinedev/core";

const MyRoute = () => {
  // If the user is not authenticated, they will be redirected to the `/login` route.
  return (
    <Authenticated key="my-routes" redirectOnFail="/login">
      <div>Authenticated</div>
    </Authenticated>
  );
};
```

## Envolver rutas con `<Authenticated />`

Ahora actualizaremos nuestro `src/App.tsx` con una ruta envoltorio que gestiona la autenticación y monta nuestro componente `<ListProducts />` si el usuario está autenticado. Si el usuario no está autenticado, será redirigido a la ruta `/login`.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";
// highlight-next-line
import routerProvider from "@refinedev/react-router";

// highlight-start
import { BrowserRouter, Routes, Route, Outlet, Navigate } from "react-router";
// highlight-end

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
    <BrowserRouter>
      <Refine
        dataProvider={dataProvider}
        authProvider={authProvider}
        routerProvider={routerProvider}
      >
        {/* highlight-start */}
        <Routes>
          <Route
            element={
              // We're wrapping our routes with the `<Authenticated />` component
              // We're omitting the `fallback` prop to redirect users to the login page if they are not authenticated.
              // If the user is authenticated, we'll render the `<Header />` component and the `<Outlet />` component to render the inner routes.
              <Authenticated key="authenticated-routes" redirectOnFail="/login">
                <Header />
                <Outlet />
              </Authenticated>
            }
          >
            <Route index element={<ListProducts />} />
          </Route>
          <Route
            element={
              <Authenticated key="auth-pages" fallback={<Outlet />}>
                {/* We're redirecting the user to `/` if they are authenticated and trying to access the `/login` route */}
                <Navigate to="/" />
              </Authenticated>
            }
          >
            <Route path="/login" element={<Login />} />
          </Route>
        </Routes>
        {/* highlight-end */}
      </Refine>
    </BrowserRouter>
  );
}
```

<AddAuthenticationToApp />

Ahora actualizamos nuestras rutas para gestionar la autenticación, redirigir a las rutas adecuadas según el estado de autenticación y redirigir a la ruta `/` desde la ruta índice.

En el siguiente paso aprenderemos a definir rutas e informar a Refine sobre las rutas relacionadas por cada resource.

</Sandpack>
