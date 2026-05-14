# Tanstack React Table integration for refine

`@refinedev/react-table` verbindet Refines Tabellenlogik mit [TanStack React Table](https://tanstack.com/table/v8). Das package stellt `useTable` bereit, damit Sortierung, Filterung, Pagination und Ressourcenabfragen mit einer headless Tabellenbibliothek umgesetzt werden koennen.

## Installation

```sh
npm install @refinedev/react-table @tanstack/react-table
```

## Grundlegende Verwendung

```tsx
import { useTable } from "@refinedev/react-table";

import { ColumnDef, flexRender } from "@tanstack/react-table";

const EditPost = () => {
  const tableInstance = useTable({
    columns,
    refineCoreProps: {
      resource: "posts",
    },
  });

  return; /* ... */
};
```

Dieses package eignet sich fuer Projekte, die volle Kontrolle ueber Markup und Styling brauchen, aber Refines Daten-Hooks fuer Tabellen beibehalten moechten.

Weitere Details findest du in der [TanStack React Table documentation](https://refine.dev/docs/packages/documentation/tanstack-table/introduction) und im [advanced table example](https://refine.dev/docs/examples/table/tanstack/advanced-react-table/).
