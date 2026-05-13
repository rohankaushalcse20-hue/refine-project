---
title: Obtener un registro
---

import { Sandpack, AddGetOneMethod, CreateShowProductFile, AddUseOneToShowProduct, AddShowProductToAppTsx } from "./sandpack.tsx";

<Sandpack>

En este paso aprenderemos a usar el hook `useOne` de Refine para obtener un único registro desde nuestra API e implementar el método `getOne` en nuestro data provider.

## Implementar el método `getOne`

Para obtener un registro con los hooks de Refine, primero debemos implementar el método [`getOne`](/core/docs/data/data-provider/#getone-) en nuestro data provider. Este método se llamará cuando usemos el hook [`useOne`](/core/docs/data/hooks/use-one) o sus extensiones dentro de nuestros componentes.

El método `getOne` acepta las propiedades `resource`, `id` y `meta`.

- `resource` se refiere a la entidad que estamos obteniendo.
- `id` es el ID del registro que estamos obteniendo.
- `meta` es un objeto que contiene datos adicionales pasados al hook.

Nuestra API de prueba tiene la entidad `products` y espera que obtengamos un único registro con el endpoint `/products/:id`. Por eso usaremos las propiedades `resource` e `id` para realizar la solicitud.

Actualiza tu archivo `src/providers/data-provider.ts` agregando las siguientes líneas:

```ts title="src/providers/data-provider.ts"
import type { DataProvider } from "@refinedev/core";

const API_URL = "https://api.fake-rest.refine.dev";

export const dataProvider: DataProvider = {
  // highlight-start
  getOne: async ({ resource, id, meta }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`);

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-end
  update: () => {
    throw new Error("Not implemented");
  },
  getList: () => {
    throw new Error("Not implemented");
  },
  /* ... */
};
```

<AddGetOneMethod />

## Usar el hook `useOne`

Después de implementar el método `getOne`, podremos llamar al hook `useOne` y obtener un único registro desde nuestra API. Creemos un componente llamado `ShowProduct` y montémoslo dentro de nuestro componente `<Refine />`.

<CreateShowProductFile />

Después importaremos el hook `useOne` y lo usaremos dentro de nuestro componente `ShowProduct` para obtener un único registro de la entidad `products` desde nuestra API.

Actualiza tu archivo `src/pages/products/show.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/show.tsx"
// highlight-next-line
import { useOne } from "@refinedev/core";

export const ShowProduct = () => {
  // highlight-next-line
  const {
    result,
    query: { isLoading },
  } = useOne({ resource: "products", id: 123 });

  if (isLoading) {
    return <div>Loading...</div>;
  }

  return <div>Product name: {result?.name}</div>;
};
```

<AddUseOneToShowProduct />

Por último, montaremos el componente `ShowProduct` dentro de nuestro componente `<Refine />`.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
// highlight-next-line
import { ShowProduct } from "./pages/products/show";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider}>
      {/* highlight-next-line */}
      <ShowProduct />
    </Refine>
  );
}
```

<AddShowProductToAppTsx />

Ahora deberíamos poder ver el nombre del producto en pantalla.

En el siguiente paso aprenderemos a usar el hook `useUpdate` de Refine para actualizar un único registro desde nuestra API e implementar el método `update` en nuestro data provider.

</Sandpack>
