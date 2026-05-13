---
title: Inferir parámetros
---

import { Sandpack, AddInferenceToEditProduct, AddInferenceToCreateProduct, AddInferenceToShowProduct, AddInferenceToListProducts } from "./sandpack.tsx";

<Sandpack>

Ahora aprendimos sobre el hook `useNavigation` y cómo gestionar la navegación con Refine. En este paso actualizaremos los componentes para aprovechar la inferencia de parámetros de Refine.

Cuando se integra con un router provider, Refine infiere los parámetros desde las definiciones de ruta y los incorpora en sus hooks y componentes, eliminando la necesidad de pasar manualmente parámetros `resource`, `id` y `action`.

:::tip

Siempre puedes pasar los parámetros manualmente si quieres sobrescribir los parámetros inferidos.

:::

## Actualizar el componente `ListProducts`

Actualicemos nuestro componente `<ListProducts />` y omitamos el parámetro `resource` del hook `useTable`.

Actualiza tu archivo `src/pages/products/list.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/list.tsx"
import { useTable, useMany } from "@refinedev/core";

export const ListProducts = () => {
  const {
    tableQuery: { isLoading },
    currentPage,
    setCurrentPage,
    pageCount,
    sorters,
    setSorters,
  } = useTable({
    // removed-line
    resource: "products",
    pagination: { currentPage: 1, pageSize: 10 },
    sorters: { initial: [{ field: "id", order: "asc" }] },
  });

  /* ... */
};
```

<AddInferenceToListProducts />

## Actualizar el componente `ShowProduct`

Actualicemos nuestro componente `<ShowProduct />` y omitamos los parámetros `resource` e `id`. Recuerda que antes habíamos fijado el parámetro `id` de forma manual. Ahora dejaremos que Refine infiera el parámetro `id` desde la definición de ruta y obtenga el producto dinámicamente.

También empezaremos a usar el hook [`useShow`](/core/docs/data/hooks/use-show), que es un wrapper alrededor de `useOne`. A diferencia del hook useOne, ofrece capacidades de inferencia y elimina la necesidad de pasar explícitamente los parámetros `resource` e `id`.

Actualiza tu archivo `src/pages/products/show.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/show.tsx"
// highlight-next-line
import { useShow } from "@refinedev/core";

export const ShowProduct = () => {
  // removed-line
  const { isLoading } = useOne({ resource: "products", id: 123 });
  // added-line
  const { query } = useShow();

  /* ... */
};
```

<AddInferenceToShowProduct />

## Actualizar el componente `EditProduct`

Actualicemos nuestro componente `<EditProduct />` y omitamos los parámetros `resource`, `action` e `id` del hook `useForm`. Igual que con el componente `<ShowProduct />`, dejaremos que Refine infiera el parámetro `id` desde la definición de ruta. Como definimos la acción `edit` en nuestra definición de resource, Refine también inferirá el parámetro `action` como `edit`.

Actualiza tu archivo `src/pages/products/edit.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/edit.tsx"
import { useForm, useSelect } from "@refinedev/core";

export const EditProduct = () => {
  // removed-line
  const { onFinish, mutation, query } = useForm({
    // removed-line
    action: "edit",
    // removed-line
    resource: "products",
    // removed-line
    id: "123",
    // removed-line
  });
  // added-line
  const { onFinish, mutation, query } = useForm();

  /* ... */
};
```

<AddInferenceToEditProduct />

## Actualizar el componente `CreateProduct`

Actualicemos nuestro componente `<CreateProduct />` y omitamos los parámetros `resource` y `action` del hook `useForm`. Como definimos la acción `create` en nuestra definición de resource, Refine también inferirá el parámetro `action` como `create`.

Actualiza tu archivo `src/pages/products/create.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/create.tsx"
import { useForm, useSelect } from "@refinedev/core";

export const CreateProduct = () => {
  // removed-line
  const { onFinish, mutation } = useForm({
    // removed-line
    action: "create",
    // removed-line
    resource: "products",
    // removed-line
  });
  // added-line
  const { onFinish, mutation } = useForm();

  /* ... */
};
```

<AddInferenceToCreateProduct />

Ahora deberías ver que nuestros componentes funcionan como se espera. Actualizamos correctamente los componentes para aprovechar la inferencia de parámetros de Refine.

En el siguiente paso aprenderemos a gestionar redirecciones en nuestra app.

</Sandpack>
