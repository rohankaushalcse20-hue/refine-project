---
title: Introdução
---

import { Sandpack, AddRouterProviderToApp } from "./sandpack.tsx";

<Sandpack>

Agora já aprendemos os fundamentos de data fetching e os conceitos básicos de autenticação no Refine. Nesta unidade, veremos como adicionar um router provider ao app e quais recursos são liberados com essa integração.

O Refine oferece integrações para as opções de routing mais populares, como [React Router](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) e [Remix](/core/docs/routing/integrations/remix).

:::simple Dicas de implementação

- Recomendamos escolher uma integração nativa para o seu roteador, mas, se você quiser usar uma solução customizada, pode criar seu próprio provider com a [interface de router provider](/core/docs/routing/router-provider) do Refine, que é simples de usar.

- O Refine não interfere na forma como seu roteador lida com navegação. Você continuará gerando rotas e páginas como faria normalmente no roteador escolhido.

- Fornecer um router provider ao Refine libera muitos recursos sem abrir mão das funcionalidades do seu roteador.

:::

Esta unidade cobre os seguintes tópicos:

- O conceito de resource no Refine e como usá-lo,
- Usar a integração de router para inferir parâmetros como `resource`, `action` e `id` a partir da URL,
- Lidar com navegação e redirecionamentos no Refine,
- Usar a integração de router para armazenar estados de formulários e tabelas na URL,
- Por fim, lidar com autenticação usando opções do router.

Esta unidade é independente de UI framework. As partes de routing relacionadas aos UI frameworks serão abordadas nas próximas unidades.

## Adicionando o Router Provider

Vamos começar adicionando as dependências. Para routing, usaremos `react-router`; para integrá-lo ao Refine, usaremos o pacote `@refinedev/react-router`.

<InstallPackagesCommand args="react-router @refinedev/react-router"/>

Depois, passaremos o router provider para o componente `<Refine />`. Além disso, envolveremos o app com `<BrowserRouter />` de `react-router`.

Atualize o arquivo `src/App.tsx` adicionando as seguintes linhas:

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";
// highlight-next-line
import routerProvider from "@refinedev/react-router";

// highlight-next-line
import { BrowserRouter } from "react-router";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

import { ShowProduct } from "./pages/products/show";
import { EditProduct } from "./pages/products/edit";
import { ListProducts } from "./pages/products/list";
import { CreateProduct } from "./pages/products/create";

import { Login } from "./pages/login";
import { Header } from "./components/header";

export default function App(): JSX.Element {
  return (
    // highlight-next-line
    <BrowserRouter>
      <Refine
        dataProvider={dataProvider}
        authProvider={authProvider}
        // highlight-next-line
        routerProvider={routerProvider}
      >
        <Authenticated key="protected" fallback={<Login />}>
          <Header />
          {/* <ShowProduct /> */}
          {/* <EditProduct /> */}
          <ListProducts />
          {/* <CreateProduct /> */}
        </Authenticated>
      </Refine>
      {/* highlight-next-line */}
    </BrowserRouter>
  );
}
```

<AddRouterProviderToApp />

Agora estamos prontos para explorar os recursos da integração de router do Refine.

Na próxima etapa, aprenderemos como informar ao Refine as rotas relacionadas a cada resource.

</Sandpack>
