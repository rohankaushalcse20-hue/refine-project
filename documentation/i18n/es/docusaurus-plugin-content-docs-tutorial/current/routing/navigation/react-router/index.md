---
title: Navegación
---

import { Sandpack, AddLinksToHeader, AddShowAndEditButtonsToListProducts } from "./sandpack.tsx";

<Sandpack>

Ahora configuramos nuestras rutas y resources. En este paso aprenderemos sobre los helpers de navegación de Refine y cómo usarlos en nuestra app.

:::tip

Siempre puedes usar los métodos preferidos de tu librería de routing para navegar entre páginas. Los hooks de navegación de Refine son helpers que facilitan la navegación entre cualquier acción de cualquier resource.

:::

Usaremos el hook [`useNavigation`](/core/docs/routing/hooks/use-navigation) y crearemos botones para navegar a las páginas create, edit y show de los productos. Además, proporcionaremos un enlace a la página de lista de productos en el componente `<Header />`.

## Agregar un enlace a la página de lista y a la página de creación

Usaremos el hook `useNavigation` de `@refinedev/core` y el componente `<Link />` de la librería `react-router` para crear enlaces a la página de lista y a la página de creación de productos.

Actualicemos nuestro componente `<Header />` y agreguemos un enlace a la página de lista de productos:

```tsx title="src/components/header.tsx"
import React from "react";
// highlight-next-line
import { useLogout, useGetIdentity, useNavigation } from "@refinedev/core";

// highlight-next-line
import { Link } from "react-router";

export const Header = () => {
  const {
    mutate,
    mutation: { isPending },
  } = useLogout();
  const { data: identity } = useGetIdentity();

  // You can also use methods like list or create to trigger navigation.
  // We're using url methods to provide more semantically correct html.
  // highlight-next-line
  const { listUrl, createUrl } = useNavigation();

  return (
    <>
      <h2>
        <span>Welcome, </span>
        <span>{identity?.name ?? ""}</span>
      </h2>
      {/* highlight-start */}
      <Link to={listUrl("protected-products")}>List Products</Link>
      <Link to={createUrl("protected-products")}>Create Product</Link>
      {/* highlight-end */}
      <button type="button" disabled={isPending} onClick={mutate}>
        Logout
      </button>
    </>
  );
};
```

<AddLinksToHeader />

## Agregar botones Show y Edit a la página de lista

De forma similar, actualizaremos el componente `<ListProducts />` y agregaremos enlaces para mostrar y editar los productos.

```tsx title="src/pages/products/list.tsx"
// highlight-next-line
import { useTable, useMany, useNavigation } from "@refinedev/core";

// highlight-next-line
import { Link } from "react-router";

export const ListProducts = () => {
  const {
    result,
    tableQuery: { isLoading },
    currentPage,
    setCurrentPage,
    pageCount,
    sorters,
    setSorters,
  } = useTable({
    resource: "protected-products",
    pagination: { currentPage: 1, pageSize: 10 },
    sorters: { initial: [{ field: "id", order: "asc" }] },
  });

  // You can also use methods like show or list to trigger navigation.
  // We're using url methods to provide more semantically correct html.
  // highlight-next-line
  const { showUrl, editUrl } = useNavigation();

  /* ... */

  return (
    <div>
      <h1>Products</h1>
      <table>
        <thead>
          <tr>
            <th onClick={() => onSort("id")}>
              ID {indicator[getSorter("id")]}
            </th>
            <th onClick={() => onSort("name")}>
              Name {indicator[getSorter("name")]}
            </th>
            <th>Category</th>
            <th onClick={() => onSort("material")}>
              Material {indicator[getSorter("material")]}
            </th>
            <th onClick={() => onSort("price")}>
              Price {indicator[getSorter("price")]}
            </th>
            {/* highlight-start */}
            <th>Actions</th>
            {/* highlight-end */}
          </tr>
        </thead>
        <tbody>
          {result?.data?.map((product) => (
            <tr key={product.id}>
              <td>{product.id}</td>
              <td>{product.name}</td>
              <td>
                {
                  categories?.data?.find(
                    (category) => category.id == product.category?.id,
                  )?.title
                }
              </td>
              <td>{product.material}</td>
              <td>{product.price}</td>
              {/* highlight-start */}
              <td>
                <Link to={showUrl("protected-products", product.id)}>Show</Link>
                <Link to={editUrl("protected-products", product.id)}>Edit</Link>
              </td>
              {/* highlight-end */}
            </tr>
          ))}
        </tbody>
      </table>
      <div className="pagination">{/* ... */}</div>
    </div>
  );
};
```

<AddShowAndEditButtonsToListProducts />

:::info

También puedes usar anchors y cualquier otro método de navegación que proporcione tu librería de routing para moverte entre páginas, sin limitarte al hook `useNavigation`.

:::

Ahora aprendimos a navegar entre páginas con el hook `useNavigation` de Refine. En el siguiente paso actualizaremos nuestros componentes para aprovechar la inferencia de parámetros de Refine.

</Sandpack>
