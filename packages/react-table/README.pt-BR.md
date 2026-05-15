# Integracao TanStack React Table para refine

`@refinedev/react-table` conecta os hooks de dados do Refine ao [TanStack React Table](https://tanstack.com/table/v8). Ele ajuda a montar tabelas headless com paginacao, filtros, ordenacao e estado sincronizados com os resources.

## Instalacao

```sh
npm install @refinedev/react-table @tanstack/react-table
```

## Uso basico

```tsx
import { useTable } from "@refinedev/react-table";

const table = useTable({
  columns,
  refineCoreProps: {
    resource: "posts",
  },
});
```

## Quando usar

Use este pacote quando voce quiser controlar markup, estilos e componentes da tabela, mantendo o Refine responsavel por buscar dados e gerenciar estado de CRUD.

## Documentacao

- Consulte a [documentacao do TanStack Table com refine](https://refine.dev/docs/packages/documentation/tanstack-table/introduction).
- Veja o [exemplo avancado com TanStack React Table](https://refine.dev/docs/examples/table/tanstack/advanced-react-table/).
