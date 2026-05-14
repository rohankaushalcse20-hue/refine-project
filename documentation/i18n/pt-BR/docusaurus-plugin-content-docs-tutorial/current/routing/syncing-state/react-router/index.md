---
title: Sincronizando estado com a location
---

import { Sandpack, AddLocationSyncToListProducts } from "./sandpack.tsx";

<Sandpack>

Como etapa final desta unidade, aprenderemos a sincronizar o estado das tabelas com a location. Isso permite compartilhar o estado `currentPage` da tabela com outras pessoas. Por exemplo, podemos enviar a URL da tabela para colegas, e eles verão a mesma tabela com os mesmos filtros, ordenação e paginação.

O hook `useTable` do Refine oferece a opção `syncWithLocation`, que permite sincronizar o estado da tabela com a location usando uma única linha de código.

Sempre que o estado da tabela mudar, como filtros, ordenação ou paginação, a URL será atualizada com o novo estado. Quando a página for carregada, a tabela será atualizada com o estado presente na URL.

Vamos atualizar o componente `<ListProducts>` e adicionar a opção `syncWithLocation` ao hook `useTable`.

Atualize o arquivo `src/pages/products/list.tsx` adicionando as seguintes linhas:

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

Agora, tente navegar até a página `/products` e alterar filtros, ordenação ou paginação. Você verá que a URL é atualizada com o novo estado da tabela. Ao recarregar a página, a tabela será atualizada com o mesmo estado da URL.

## Resumo

Nesta unidade, aprendemos:

- Como usar as integrações de router do Refine,
- Como definir resources e por que isso é importante,
- Como usar parâmetros inferidos da URL nos hooks,
- Como usar hooks do Refine para lidar com navegação entre ações de qualquer resource,
- Como lidar com redirecionamentos vindos do auth provider e de formulários,
- Como sincronizar o estado da tabela com a location.

Na próxima unidade, aprenderemos como usar um UI framework com o Refine e como o Refine lida com integrações de UI framework.

</Sandpack>
