---
title: Buscando um registro
---

import { Sandpack, AddGetOneMethod, CreateShowProductFile, AddUseOneToShowProduct, AddShowProductToAppTsx } from "./sandpack.tsx";

<Sandpack>

Nesta etapa, aprenderemos a usar o hook `useOne` do Refine para buscar um único registro da nossa API e implementar o método `getOne` no data provider.

## Implementando o método `getOne`

Para buscar um registro com os hooks do Refine, primeiro precisamos implementar o método [`getOne`](/core/docs/data/data-provider/#getone-) no data provider. Esse método será chamado quando usarmos o hook [`useOne`](/core/docs/data/hooks/use-one) ou suas extensões nos componentes.

O método `getOne` aceita as propriedades `resource`, `id` e `meta`.

- `resource` representa a entidade que estamos buscando.
- `id` é o ID do registro que estamos buscando.
- `meta` é um objeto com dados adicionais passados ao hook.

Nossa fake API tem a entidade `products` e espera que busquemos um único registro pelo endpoint `/products/:id`. Por isso, usaremos as propriedades `resource` e `id` para fazer a requisição.

Atualize o arquivo `src/providers/data-provider.ts` adicionando as seguintes linhas:

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

## Usando o hook `useOne`

Depois de implementar o método `getOne`, poderemos chamar o hook `useOne` e buscar um único registro da API. Vamos criar um componente chamado `ShowProduct` e montá-lo dentro do componente `<Refine />`.

<CreateShowProductFile />

Em seguida, importaremos o hook `useOne` e o usaremos dentro do componente `ShowProduct` para buscar um único registro da entidade `products`.

Atualize o arquivo `src/pages/products/show.tsx` adicionando as seguintes linhas:

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

Por fim, montaremos o componente `ShowProduct` dentro do componente `<Refine />`.

Atualize o arquivo `src/App.tsx` adicionando as seguintes linhas:

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

Agora devemos conseguir ver o nome do produto na tela.

Na próxima etapa, aprenderemos a usar o hook `useUpdate` do Refine para atualizar um único registro da API e a implementar o método `update` no data provider.

</Sandpack>
