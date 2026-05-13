---
title: Sincronizar estado con la ubicación
---

import { Sandpack, AddLocationSyncToListProducts } from "./sandpack.tsx";

<Sandpack>

Como paso final de esta unidad, aprenderemos a sincronizar el estado de nuestras tablas con la ubicación. Esto nos permitirá compartir con otras personas el estado `currentPage` de la tabla. Por ejemplo, podemos compartir la URL de la tabla con colegas y verán la misma tabla con los mismos filtros, ordenamiento y paginación.

El hook `useTable` de Refine ofrece una opción `syncWithLocation` que nos permite sincronizar el estado de la tabla con la ubicación con una sola línea de código.

Cada vez que cambie el estado de la tabla (por ejemplo, filtros, ordenamiento o paginación), la URL se actualizará con el nuevo estado. Y la tabla se actualizará con el estado de la URL cuando se cargue la página.

Actualicemos nuestro componente `<ListProducts>` y agreguemos la opción `syncWithLocation` al hook `useTable`.

Actualiza tu archivo `src/pages/products/list.tsx` agregando las siguientes líneas:

```tsx title="src/pages/products/list.tsx"
import { useTable, useMany, useNavigation } from "@refinedev/core";

export const ListProducts = () => {
  const {
    tableQuery: { isLoading },
    currentPage,
    setCurrentPage,
    pageCount,
    sorters,
    setSorters,
  } = useTable({
    pagination: { currentPage: 1, pageSize: 10 },
    sorters: { initial: [{ field: "id", order: "asc" }] },
    // highlight-next-line
    syncWithLocation: true,
  });

  /* ... */
};
```

<AddLocationSyncToListProducts />

Ahora intentemos navegar a la página `/products` y cambiar los filtros, el ordenamiento o la paginación. Verás que la URL se actualiza con el nuevo estado de la tabla. Cuando refresques la página, verás que la tabla se actualiza con el mismo estado de la URL.

## Resumen

En esta unidad aprendimos:

- Cómo usar las integraciones de router de Refine,
- Cómo definir resources y por qué es importante definirlos,
- Usar los parámetros inferidos desde la URL en nuestros hooks,
- Usar los hooks de Refine para gestionar la navegación entre cualquier acción de cualquier resource,
- Gestionar redirecciones desde el auth provider y los formularios,
- Sincronizar el estado de la tabla con la ubicación.

En la siguiente unidad aprenderemos cómo usar un framework UI con Refine y cómo Refine gestiona las integraciones de frameworks UI.

</Sandpack>
