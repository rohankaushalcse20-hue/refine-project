---
title: Protegendo conteúdo
---

import { Sandpack, CreateAuthProviderFile, AddAuthProviderToAppTsx, AddCheckMethodToAuthProvider, AddAuthenticatedComponentToAppTsx } from "./sandpack.tsx";

<Sandpack>

Nesta etapa, implementaremos um `authProvider` básico com o método `check` para validar o status de autenticação do usuário, permitindo proteger nosso conteúdo de usuários não autenticados.

O Refine funciona com qualquer solução de autenticação por meio da interface `authProvider`, que é simples de implementar. Vamos criar uma implementação para nossa fake REST API, que também oferece endpoints simples de autenticação.

Para saber mais sobre os auth providers disponíveis, consulte a seção [Supported Authentication Providers](/core/docs/guides-concepts/authentication/#supported-auth-providers) no guia de Authentication.

## Criando um Auth Provider

Implementaremos cada método passo a passo, cobrindo os detalhes necessários.

Primeiro, criaremos um arquivo `src/providers/auth-provider.ts` no projeto. Ele conterá todos os métodos que precisamos implementar para o nosso auth provider.

<CreateAuthProviderFile />

Depois, passaremos nosso auth provider para o componente `<Refine />` no arquivo `src/App.tsx` usando a prop `authProvider`.

Atualize o arquivo `src/App.tsx` adicionando as seguintes linhas:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
// highlight-next-line
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

export default function App(): JSX.Element {
  return (
    <Refine
      dataProvider={dataProvider}
      // highlight-next-line
      authProvider={authProvider}
    >
      {/* <ShowProduct /> */}
      {/* <EditProduct /> */}
      <ListProducts />
      {/* <CreateProduct /> */}
    </Refine>
  );
}
```

<AddAuthProviderToAppTsx />

## Implementando o método `check`

O método `check` é usado pelo hook `useIsAuthenticated` e pelo componente `<Authenticated />` para verificar o status de autenticação do usuário. Ele deve retornar uma `Promise` que resolve para um objeto.

Se o usuário estiver autenticado, o objeto deve conter a propriedade `authenticated: true`. Caso contrário, deve conter `authenticated: false`.

Obteremos um token de acesso por meio do método `login` da nossa API e o armazenaremos no local storage. Agora vamos verificar se esse token existe no local storage.

Atualize o arquivo `src/providers/auth-provider.ts` adicionando as seguintes linhas:

```ts title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  // highlight-start
  check: async () => {
    // When logging in, we'll obtain an access token from our API and store it in the local storage.
    // Now let's check if the token exists in the local storage.
    // In the later steps, we'll be implementing the `login` and `logout` methods.
    const token = localStorage.getItem("my_access_token");

    return { authenticated: Boolean(token) };
  },
  // highlight-end
  login: async ({ email, password }) => {
    throw new Error("Not implemented");
  },
  logout: async () => {
    throw new Error("Not implemented");
  },
  onError: async (error) => {
    throw new Error("Not implemented");
  },
  // ...
};
```

<AddCheckMethodToAuthProvider />

## Usando o componente `<Authenticated />`

Depois de implementar o método `check`, poderemos usar o componente `<Authenticated />` para proteger nosso conteúdo de usuários não autenticados.

Vamos adicionar o componente `<Authenticated />` ao arquivo `src/App.tsx` e envolver nosso conteúdo dentro do componente `<Refine />`.

Atualize o arquivo `src/App.tsx` adicionando as seguintes linhas:

```tsx title="src/App.tsx"
// highlight-next-line
import { Refine, Authenticated } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider} authProvider={authProvider}>
      {/* highlight-start */}
      <Authenticated key="protected" fallback={<div>Not authenticated</div>}>
        {/* <ShowProduct /> */}
        {/* <EditProduct /> */}
        <ListProducts />
        {/* <CreateProduct /> */}
      </Authenticated>
      {/* highlight-end */}
    </Refine>
  );
}
```

<AddAuthenticatedComponentToAppTsx />

:::note

Observe que adicionamos a prop `key` ao componente `<Authenticated />`. Isso é necessário para que o componente funcione corretamente, especialmente quando ele é usado várias vezes na mesma árvore de renderização.

:::

Agora você deve conseguir ver o componente `<Authenticated />` em ação. Nosso conteúdo não será renderizado; em vez disso, a prop `fallback` será renderizada.

:::tip

Você também pode usar o hook `useIsAuthenticated`, que é usado internamente pelo componente `<Authenticated />`. Saiba mais na documentação do hook [useIsAuthenticated](/core/docs/authentication/hooks/use-is-authenticated/).

:::

Na próxima etapa, implementaremos as funcionalidades de login e logout para fazer o método `check` funcionar corretamente.

</Sandpack>
