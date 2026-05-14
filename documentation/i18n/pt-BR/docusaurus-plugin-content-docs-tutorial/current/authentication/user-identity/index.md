---
title: Usando a identidade do usuário
---

import { Sandpack, AddGetIdentityMethodToAuthProvider, AddUseGetIdentityToHeaderComponent } from "./sandpack.tsx";

<Sandpack>

Nas etapas anteriores, adicionamos funcionalidades de login e logout e protegemos nosso conteúdo de usuários não autenticados. Agora aprenderemos a usar o hook `useGetIdentity` do Refine para obter a identidade do usuário pela API e implementar o método `getIdentity` no auth provider.

Implementaremos um componente simples chamado `UserGreeting` para exibir uma mensagem de boas-vindas ao usuário.

## Implementando o método `getIdentity`

O método `getIdentity` é usado para obter a identidade do usuário pela API. Ele deve retornar uma `Promise` que resolve para um objeto. Esse objeto deve conter a identidade do usuário.

Nossa fake REST API exige o envio de uma requisição `GET` para o endpoint `/auth/me` com o `token` no header `Authorization`. Ela retornará a identidade do usuário no corpo da resposta.

Atualize o arquivo `src/providers/auth-provider.ts` adicionando as seguintes linhas:

```ts title="src/providers/auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  // highlight-start
  getIdentity: async () => {
    const response = await fetch("https://api.fake-rest.refine.dev/auth/me", {
      headers: {
        Authorization: localStorage.getItem("my_access_token"),
      },
    });

    if (response.status < 200 || response.status > 299) {
      return null;
    }

    const data = await response.json();

    return data;
  },
  // highlight-end
  logout: async () => {
    /* ... */
  },
  login: async ({ email, password }) => {
    /* ... */
  },
  check: async () => {
    /* ... */
  },
  onError: async (error) => {
    /* ... */
  },
  // ...
};
```

<AddGetIdentityMethodToAuthProvider />

## Usando o hook `useGetIdentity`

Depois de implementar o método `getIdentity`, poderemos chamar o hook `useGetIdentity` e obter a identidade do usuário pela API.

Agora usaremos o hook `useGetIdentity` dentro do componente `<Header />` para cumprimentar o usuário.

Atualize o arquivo `src/components/header.tsx` adicionando as seguintes linhas:

```tsx title="src/components/header.tsx"
import React from "react";
import { useLogout, useGetIdentity } from "@refinedev/core";

export const Header = () => {
  const { mutate, isPending } = useLogout();
  const { data: identity } = useGetIdentity();

  return (
    <>
      <h2>
        <span>Welcome, </span>
        <span>{identity?.name ?? ""}</span>
      </h2>
      <button type="button" disabled={isPending} onClick={mutate}>
        Logout
      </button>
    </>
  );
};
```

<AddUseGetIdentityToHeaderComponent />

Agora, ao fazer login, devemos ver uma mensagem de boas-vindas com o nome do usuário na tela.

:::simple Note

Para fins de demonstração, nossa fake REST API retorna "John Doe" como nome do usuário, independentemente do token enviado.

:::

Neste ponto, configuramos o fluxo básico de autenticação. Na próxima etapa, aprenderemos como integrá-lo ao data provider.

</Sandpack>
