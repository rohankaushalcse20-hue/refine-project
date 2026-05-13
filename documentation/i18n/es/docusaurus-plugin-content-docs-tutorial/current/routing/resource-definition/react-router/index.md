---
title: Definir resources
---

import { Sandpack, AddRoutesToApp, AddResourcesToApp } from "./sandpack.tsx";

<Sandpack>

Hasta ahora integramos la lógica de autenticación en nuestras rutas. En este paso crearemos rutas para estos componentes y definiremos nuestros resources para informar a Refine sobre sus rutas correspondientes.

Para obtener más información, consulta la sección [Resource Concept](/core/docs/guides-concepts/general-concepts/#resource-concept) de la guía General Concepts.

## Crear rutas

En el paso anterior envolvimos nuestras rutas con el componente [`<Authenticated />`](/core/docs/authentication/components/authenticated). Ahora crearemos rutas bajo el path `/products` para ubicar nuestros componentes.
Usaremos las siguientes rutas para ubicar nuestros componentes:

- `/products` - `<ListProducts />`
- `/products/:id` - `<ShowProduct />`
- `/products/:id/edit` - `<EditProduct />`
- `/products/create` - `<CreateProduct />`

También definiremos una ruta índice en `/` y la redirigiremos a `/products` usando el componente `<Navigate />`.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";

import { BrowserRouter, Routes, Route, Outlet, Navigate } from "react-router";

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
        <Routes>
          <Route
            element={
              <Authenticated key="authenticated-routes" redirectOnFail="/login">
                <Header />
                <Outlet />
              </Authenticated>
            }
          >
            {/* highlight-start */}
            <Route index element={<Navigate to="/products" />} />
            <Route path="/products">
              <Route index element={<ListProducts />} />
              <Route path=":id" element={<ShowProduct />} />
              <Route path=":id/edit" element={<EditProduct />} />
              <Route path="create" element={<CreateProduct />} />
            </Route>
            {/* highlight-end */}
          </Route>
          <Route
            element={
              <Authenticated key="auth-pages" fallback={<Outlet />}>
                {/* highlight-start */}
                <Navigate to="/products" />
                {/* highlight-end */}
              </Authenticated>
            }
          >
            <Route path="/login" element={<Login />} />
          </Route>
        </Routes>
      </Refine>
    </BrowserRouter>
  );
}
```

<AddRoutesToApp />

## Definir resources

Ahora que creamos nuestras rutas, es momento de definir nuestros resources. Esto permitirá que Refine conozca nuestros resources y los trate de forma adecuada.

Aunque definir resources y asignar rutas apropiadas a las acciones es opcional, se recomienda hacerlo para aprovechar las funcionalidades que Refine ofrece.

Al definir nuestros resources habilitaremos estas funcionalidades:

- Inferir los parámetros relacionados desde las rutas sin tener que pasarlos explícitamente.
- Gestionar redirecciones automáticamente y navegar fácilmente entre estas rutas.
- Crear menús y breadcrumbs para nuestros resources con facilidad.
- Pasar valores `meta` a cada data hook por resource desde un único lugar.
- Gestionar fácilmente funciones como access control, i18n y más.

Usaremos la prop [`resources`](/core/docs/core/refine-component/#resources) del componente `<Refine />` para definir nuestros resources.

Una definición de resource está formada por las siguientes propiedades:

- `name`: El nombre del resource. Se pasará a los métodos del data provider para identificar el resource.
- `identifier`: Un identificador opcional para el resource. Si no se proporciona, se usará `name` como identificador. Esto es útil cuando quieres usar el mismo resource para el data provider pero tener una configuración distinta del lado de Refine.
- `list`, `create`, `edit` y `show`: Estas propiedades se usan para definir las rutas de las acciones correspondientes. Serán los valores de string de las rutas que creamos en el paso anterior.
- `meta`: Un objeto opcional para pasar valores meta por resource. Se usa ampliamente en los hooks y componentes de Refine para varios propósitos, desde data fetching, access control e i18n hasta personalización UI.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";
import routerProvider, { NavigateToResource } from "@refinedev/react-router";

import { BrowserRouter, Routes, Route, Outlet } from "react-router";

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
        // highlight-start
        resources={[
          {
            name: "protected-products",
            list: "/products",
            show: "/products/:id",
            edit: "/products/:id/edit",
            create: "/products/create",
            meta: { label: "Products" },
          },
        ]}
        // highlight-end
      >
        <Routes>
          <Route
            element={
              <Authenticated key="authenticated-routes" redirectOnFail="/login">
                <Header />
                <Outlet />
              </Authenticated>
            }
          >
            <Route
              index
              // highlight-start
              // We're also replacing the <Navigate /> component with the <NavigateToResource /> component.
              // It's tailored version of the <Navigate /> component that will redirect to the resource's list route.
              element={<NavigateToResource resource="protected-products" />}
              // highlight-end
            />
            <Route path="/products">
              <Route index element={<ListProducts />} />
              <Route path=":id" element={<ShowProduct />} />
              <Route path=":id/edit" element={<EditProduct />} />
              <Route path="create" element={<CreateProduct />} />
            </Route>
          </Route>
          <Route
            element={
              <Authenticated key="auth-pages" fallback={<Outlet />}>
                {/* highlight-start */}
                {/* We're also replacing the <Navigate /> component with the <NavigateToResource /> component. */}
                {/* It's tailored version of the <Navigate /> component that will redirect to the resource's list route. */}
                <NavigateToResource resource="protected-products" />
                {/* highlight-end */}
              </Authenticated>
            }
          >
            <Route path="/login" element={<Login />} />
          </Route>
        </Routes>
      </Refine>
    </BrowserRouter>
  );
}
```

<AddResourcesToApp />

Ahora definimos nuestras rutas y resources, y estamos listos para empezar a refactorizar nuestros componentes para beneficiarnos de las funcionalidades que proporciona Refine.

En el siguiente paso aprenderemos sobre los helpers de navegación de Refine y cómo usarlos.

</Sandpack>
