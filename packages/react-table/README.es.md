# Integracion de TanStack React Table para Refine

`@refinedev/react-table` conecta los hooks de datos de Refine con [TanStack React Table](https://tanstack.com/table). Es una opcion headless para construir tablas con paginacion, ordenamiento y filtros controlados por Refine.

## Instalacion

```sh
npm install @refinedev/react-table @tanstack/react-table
```

## Uso basico

```tsx
import { useTable } from "@refinedev/react-table";
import { ColumnDef } from "@tanstack/react-table";

const ProductList = () => {
  const columns = React.useMemo<ColumnDef<IPost>[]>(
    () => [
      {
        id: "id",
        header: "ID",
        accessorKey: "id",
      },
      {
        id: "title",
        header: "Title",
        accessorKey: "title",
        meta: {
          filterOperator: "contains",
        },
      },
    ],
    [],
  );

  const tableInstance = useTable({
    columns,
    refineCoreProps: {
      resource: "posts",
    },
  });

  return <>{/* renderiza tableInstance con TanStack React Table */}</>;
};
```

El paquete mantiene la obtencion de datos, paginacion y filtros conectados a Refine mientras deja el renderizado de la tabla bajo tu control.

## Documentacion

Consulta la [documentacion de TanStack React Table para Refine](https://refine.dev/docs/packages/documentation/tanstack-table/introduction) para ejemplos de listas, filtros y columnas.
