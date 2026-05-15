# TanStack React Table integration for refine

`@refinedev/react-table` refine के table state, pagination, sorting और filtering workflows को [TanStack React Table](https://tanstack.com/table/v8) के साथ जोड़ता है। TanStack React Table headless है, इसलिए markup और styling आप अपने design system से नियंत्रित कर सकते हैं।

## Installation

```sh
npm install @refinedev/react-table @tanstack/react-table
```

## Basic usage

```tsx
import { useTable } from "@refinedev/react-table";
import { ColumnDef } from "@tanstack/react-table";

const columns: ColumnDef<IPost>[] = [
  {
    id: "title",
    header: "Title",
    accessorKey: "title",
  },
];

const table = useTable({
  columns,
  refineCoreProps: {
    resource: "posts",
  },
});
```

जब आपको refine data provider से आने वाले records पर custom table UI बनानी हो, तब यह package TanStack table instance और refine query state को साथ रखता है।

अधिक जानकारी के लिए [TanStack React Table documentation](https://refine.dev/docs/packages/documentation/tanstack-table/introduction) और [advanced table example](https://refine.dev/docs/examples/table/tanstack/advanced-react-table/) देखें।
