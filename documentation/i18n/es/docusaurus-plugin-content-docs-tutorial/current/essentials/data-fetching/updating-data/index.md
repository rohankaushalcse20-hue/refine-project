---
title: Actualizar un registro
---

import { Sandpack, AddUpdateMethod, CreateEditProductFile, AddUseUpdateToEditProduct, AddEditProductToAppTsx } from "./sandpack.tsx";

<Sandpack>

En este paso aprenderemos a usar el hook `useUpdate` de Refine para actualizar un registro desde nuestra API e implementar el método `update` en nuestro data provider.

## Implementar el método `update`

Para actualizar un registro con los hooks de Refine, primero debemos implementar el método [`update`](/core/docs/data/data-provider/#update-) en nuestro data provider. Este método se llamará cuando usemos el hook [`useUpdate`](/core/docs/data/hooks/use-update) o sus extensiones en nuestros componentes.

El método `update` acepta las propiedades `resource`, `id`, `variables` y `meta`.

- `resource` se refiere a la entidad que estamos actualizando
- `id` es el ID del registro que estamos actualizando
- `variables` es un objeto que contiene los datos que enviamos a la API.
- `meta` es un objeto que contiene datos adicionales pasados al hook.

La entidad `products` de nuestra API de prueba espera que actualicemos un registro mediante el endpoint `/products/:id` con una solicitud `PATCH`. Por eso usaremos las propiedades `resource`, `id` y `variables` para realizar la solicitud.

Actualiza tu archivo `src/providers/data-provider.ts` agregando las siguientes líneas:

```ts title="src/providers/data-provider.ts"
import type { DataProvider } from "@refinedev/core";

const API_URL = "https://api.fake-rest.refine.dev";

export const dataProvider: DataProvider = {
  getOne: async ({ resource, id, meta }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`);

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-start
  update: async ({ resource, id, variables }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`, {
      method: "PATCH",
      body: JSON.stringify(variables),
      headers: {
        "Content-Type": "application/json",
      },
    });

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-end
  getList: () => {
    throw new Error("Not implemented");
  },
  /* ... */
};
```

<AddUpdateMethod />

## Usar el hook `useUpdate`

Después de implementar el método `update`, podremos llamar al hook `useUpdate` y actualizar un único registro desde nuestra API. Creemos un componente llamado `EditProduct` y montémoslo dentro de nuestro componente `<Refine />`.

<CreateEditProductFile />

Inicialmente incluiremos una llamada al hook `useOne` en nuestro componente `EditProduct` para obtener el registro que queremos actualizar.

Luego usaremos el hook `useUpdate` dentro de `EditProduct` para actualizar un único registro de la entidad `products` desde nuestra API.

Actualiza tu archivo `src/pages/products/edit.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/edit.tsx"
// highlight-next-line
import { useOne, useUpdate } from "@refinedev/core";

export const EditProduct = () => {
  const {
    result,
    query: { isLoading },
  } = useOne({ resource: "products", id: 123 });
  // highlight-next-line
  const {
    mutate,
    mutation: { isPending: isUpdating },
  } = useUpdate();

  if (isLoading) {
    return <div>Loading...</div>;
  }

  const updatePrice = async () => {
    // highlight-start
    await mutate({
      resource: "products",
      id: 123,
      values: {
        price: Math.floor(Math.random() * 100),
      },
    });
    // highlight-end
  };

  return (
    <div>
      <div>Product name: {result?.name}</div>
      <div>Product price: ${result?.price}</div>
      <button onClick={updatePrice}>Update Price</button>
    </div>
  );
};
```

<AddUseUpdateToEditProduct />

Por último, montaremos nuestro componente `EditProduct` dentro de nuestro componente `<Refine />`.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";

import { ShowProduct } from "./pages/products/show";
// highlight-next-line
import { EditProduct } from "./pages/products/edit";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider}>
      {/* <ShowProduct /> */}
      {/* highlight-next-line */}
      <EditProduct />
    </Refine>
  );
}
```

<AddEditProductToAppTsx />

Ahora deberíamos poder ver tanto el nombre como el precio del producto en pantalla. Cuando hagamos clic en el botón `Update Price`, el precio del producto se actualizará.

:::tip Invalidaciones inteligentes

Observa que cuando actualizamos el precio con `useUpdate`, el hook `useOne` que llamamos antes se invalida automáticamente. Esto ocurre porque Refine invalidará todas las queries que usan el mismo resource e id cuando actualicemos un registro. Así siempre veremos los datos más recientes en pantalla y no tendremos que invalidar las queries manualmente.

:::

En el siguiente paso aprenderemos a usar el hook `useList` de Refine para obtener una lista de registros desde nuestra API e implementar el método `getList` en nuestro data provider.

</Sandpack>
