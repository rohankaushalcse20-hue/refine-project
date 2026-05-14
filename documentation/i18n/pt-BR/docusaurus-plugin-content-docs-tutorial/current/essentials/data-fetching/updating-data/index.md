---
title: Atualizando um registro
---

import { Sandpack, AddUpdateMethod, CreateEditProductFile, AddUseUpdateToEditProduct, AddEditProductToAppTsx } from "./sandpack.tsx";

<Sandpack>

Nesta etapa, aprenderemos a usar o hook `useUpdate` do Refine para atualizar um registro da nossa API e implementar o método `update` no data provider.

## Implementando o método `update`

Para atualizar um registro com os hooks do Refine, primeiro precisamos implementar o método [`update`](/core/docs/data/data-provider/#update-) no data provider. Esse método será chamado quando usarmos o hook [`useUpdate`](/core/docs/data/hooks/use-update) ou suas extensões nos componentes.

O método `update` aceita as propriedades `resource`, `id`, `variables` e `meta`.

- `resource` representa a entidade que estamos atualizando
- `id` é o ID do registro que estamos atualizando
- `variables` é um objeto com os dados enviados para a API.
- `meta` é um objeto com dados adicionais passados ao hook.

A entidade `products` da nossa fake API espera que atualizemos um registro pelo endpoint `/products/:id` usando uma requisição `PATCH`. Por isso, usaremos as propriedades `resource`, `id` e `variables` para fazer a requisição.

Atualize o arquivo `src/providers/data-provider.ts` adicionando as seguintes linhas:

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

## Usando o hook `useUpdate`

Depois de implementar o método `update`, poderemos chamar o hook `useUpdate` e atualizar um único registro da API. Vamos criar um componente chamado `EditProduct` e montá-lo dentro do componente `<Refine />`.

<CreateEditProductFile />

Inicialmente, incluiremos uma chamada ao hook `useOne` no componente `EditProduct` para buscar o registro que queremos atualizar.

Depois, usaremos o hook `useUpdate` dentro de `EditProduct` para atualizar um único registro da entidade `products`.

Atualize o arquivo `src/pages/products/edit.tsx` adicionando as seguintes linhas:

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

Por fim, montaremos o componente `EditProduct` dentro do componente `<Refine />`.

Atualize o arquivo `src/App.tsx` adicionando as seguintes linhas:

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

Agora devemos conseguir ver o nome e o preço do produto na tela. Ao clicar no botão `Update Price`, o preço do produto será atualizado.

:::tip Invalidações inteligentes

Observe que, quando atualizamos o preço usando `useUpdate`, o hook `useOne` chamado anteriormente é invalidado automaticamente. Isso acontece porque o Refine invalida todas as queries que usam o mesmo resource e id quando atualizamos um registro. Assim, veremos sempre os dados mais recentes na tela sem precisar invalidar queries manualmente.

:::

Na próxima etapa, aprenderemos a usar o hook `useList` do Refine para buscar uma lista de registros da API e a implementar o método `getList` no data provider.

</Sandpack>
