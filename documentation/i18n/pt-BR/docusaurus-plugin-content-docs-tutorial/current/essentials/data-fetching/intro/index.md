---
title: Data Fetching
---

import { Sandpack, FocusOnDataProviderFile, AddDataProviderToRefine } from "./sandpack.tsx";

<Sandpack>

Nesta etapa, aprenderemos os fundamentos de data fetching no Refine. O componente `<Refine />` aceita a prop [`dataProvider`](/core/docs/core/refine-component/#dataprovider-), usada para lidar com todas as operações de busca e mutação de dados por meio de uma interface simples. Embora o Refine ofereça vários data providers prontos, neste tutorial criaremos nosso próprio data provider e o conectaremos a uma [fake REST API](https://api.fake-rest.refine.dev/).

Para saber mais sobre os data providers disponíveis, consulte a seção [Supported Data Providers](/core/docs/guides-concepts/data-fetching/#supported-data-providers) no guia de Data Fetching.

## Criando um Data Provider

Implementaremos cada método passo a passo, cobrindo os detalhes necessários. Usaremos `fetch` para as requisições de API, mas você pode escolher qualquer biblioteca.

Primeiro, criaremos um arquivo `src/providers/data-provider.ts` no projeto. Ele conterá todos os métodos que precisamos implementar para o nosso data provider.

Para ver um data provider vazio, <FocusOnDataProviderFile>confira o arquivo `src/providers/data-provider.ts`</FocusOnDataProviderFile> no painel à direita.

Depois, passaremos nosso data provider para o componente `<Refine />` no arquivo `src/App.tsx` usando a prop `dataProvider`.

Atualize o arquivo `src/App.tsx` adicionando as seguintes linhas:

```tsx
import { Refine, WelcomePage } from "@refinedev/core";

// highlight-next-line
import { dataProvider } from "./providers/data-provider";

export default function App(): JSX.Element {
  return (
    // highlight-next-line
    <Refine dataProvider={dataProvider}>
      <WelcomePage />
    </Refine>
  );
}
```

<AddDataProviderToRefine />

:::tip

Também é possível usar múltiplos data providers com o Refine. Saiba mais na seção [Multiple Data Providers](/core/docs/guides-concepts/data-fetching/#multiple-data-providers) do guia de Data Fetching.

:::

Na próxima etapa, aprenderemos a buscar um registro usando o hook `useOne` do Refine e também a implementar o método `getOne` no nosso data provider.

</Sandpack>
