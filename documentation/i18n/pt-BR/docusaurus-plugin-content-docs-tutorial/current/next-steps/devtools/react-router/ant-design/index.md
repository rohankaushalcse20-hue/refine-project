---
title: Usando o Devtools
---

import { Sandpack, SelectorButtonIcon } from "./sandpack.tsx";

<Sandpack>

Nesta etapa, exploraremos o poderoso pacote Devtools do Refine, que oferece recursos de monitoramento e atualização para inspecionar e depurar aplicações Refine.

:::note

`@refinedev/devtools` está em estágio beta e em breve receberá ainda mais recursos e melhorias.

:::

O pacote `@refinedev/devtools` foi projetado para ajudar no processo de desenvolvimento e será removido dos builds de produção. Ele não terá impacto de performance na sua aplicação nem deixará código remanescente no bundle de produção.

## Instalação

A instalação do pacote é direta, mas o pacote `@refinedev/cli` também fornece um comando para instalar e configurar o Devtools. Usaremos o comando abaixo para instalar o pacote Devtools:

<Tabs>

<TabItem value="cli" label="Usando CLI" default>

```sh
npm run refine devtools init
```

</TabItem>

<TabItem value="manual" label="manual">

<InstallPackagesCommand args="@refinedev/devtools" />

Depois, precisaremos envolver a aplicação com o componente `<DevtoolsProvider />`. O componente `<DevtoolsProvider />` deve envolver o componente `<Refine />` dentro do componente `App`. Também importaremos o componente `<DevtoolsPanel />` para ter um atalho prático para abrir o Devtools na aplicação.

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";
// highlight-next-line
import { DevtoolsProvider, DevtoolsPanel } from "@refinedev/devtools";
/* ... */

export default function App() {
    return (
        {/* highlight-start */}
        {/* You can mount the DevtoolsProvider at the top most level of the element tree */}
        <DevtoolsProvider>
        {/* highlight-end */}
            <Refine>
                {/* ... */}
            </Refine>
            {/* highlight-start */}
            {/* DevtoolsPanel component should be mounted inside the DevtoolsProvider */}
            <DevtoolsPanel />
            {/* highlight-end */}
            {/* ... */}
        {/* highlight-next-line */}
        </DevtoolsProvider>
    );
}
```

Depois disso, podemos começar a usar o Devtools na aplicação.

</TabItem>

</Tabs>

## Usando o recurso de monitoramento

Depois de instalar e configurar o Devtools, você verá um pequeno painel de devtools na parte inferior da aplicação. Ao clicar nele, o Devtools será aberto. Em seguida, clique em `"Monitor"` na sidebar para abrir a tela de monitoramento.

Essa tela inclui todas as queries e mutations disparadas na aplicação durante a sessão `currentPage`. Você pode ver detalhes como resposta, data provider de destino, resource de destino, tempo de execução da query ou mutation e muito mais.

Você poderá filtrar queries e mutations por tipo, resource, status e pelo componente ou hook que as disparou. Também é possível escolher na UI o componente que deseja usar como filtro por meio do seletor.

Para usar o seletor, clique no ícone <SelectorButtonIcon />. Ao passar o mouse sobre um componente da página que disparou uma query ou mutation, ele será destacado. Clicar no componente filtrará as queries e mutations por aquele componente.

<VideoInView src="https://refine.ams3.cdn.digitaloceanspaces.com/assets/tutorial/webm/devtools-xray-3.webm" playsInline loop autoPlay muted />

## Usando o recurso de atualização

O recurso de atualização do pacote Devtools é semelhante ao comando de update do `@refinedev/cli` e oferece uma UI prática para atualizar suas dependências do Refine com um único clique. Pelo mesmo painel, você também pode adicionar novos pacotes Refine à aplicação com um clique e aprender como usá-los.

Confira a aba `"Overview"` para ver as atualizações disponíveis e clique no botão `"Add Package"` para adicionar novos pacotes Refine à aplicação.

</Sandpack>
