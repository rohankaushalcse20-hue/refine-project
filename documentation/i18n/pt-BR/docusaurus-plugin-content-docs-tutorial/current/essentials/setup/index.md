---
title: Seu primeiro app Refine
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

Criar um novo app Refine é bem simples e exige apenas alguns passos para gerar uma aplicação funcional. Para este tutorial, não usaremos todo o potencial do `create-refine-app`. Em vez disso, criaremos um app vazio, instalaremos as dependências necessárias e configuraremos a aplicação manualmente.

<Tabs wrapContent={false}>

<TabItem value="quick" label="Configuração rápida">

Para acompanhar este tutorial, você pode usar os templates iniciais fornecidos pelo `create-refine-app`. O comando abaixo criará um novo projeto vazio com os pacotes `@refinedev/core` e `@refinedev/cli`, trazendo tudo o que é necessário para começar o tutorial.

```sh
npm create refine-app@latest -- --example starter-vite
```

</TabItem>

<TabItem value="manual" label="Configuração manual">

Precisaremos criar nosso app usando os templates apropriados. Depois, instalaremos as dependências do Refine e configuraremos a aplicação.

```sh
npm create vite@latest my-refine-app -- --template react-ts
```

Para saber mais sobre o Vite e a criação de projetos, consulte a [documentação do Vite](https://vitejs.dev/guide/#scaffolding-your-first-vite-project).

Depois de criar o projeto, instalaremos as dependências do Refine.

```sh
npm install @refinedev/core @refinedev/cli
```

Estamos instalando `@refinedev/core`, que fornece todas as funcionalidades centrais do Refine, e `@refinedev/cli`, que é opcional, mas oferece vários recursos úteis para o processo de desenvolvimento. Para saber mais sobre `@refinedev/cli`, consulte [sua documentação](/core/docs/packages/cli).

### Configurando os scripts

Vamos substituir os scripts `dev`, `build` e `serve` pelos seguintes:

```json
{
  "scripts": {
    "dev": "refine dev",
    "build": "refine build",
    "serve": "refine serve"
  }
}
```

Embora os comandos runner do `refine` usem os mesmos comandos fornecidos pelo bundler, eles adicionam recursos úteis, como verificação de versões das dependências e avisos da equipe do Refine.

### Configurando o app

Precisaremos montar o componente `<Refine />` no nosso app. Vamos montá-lo na raiz da aplicação.

```tsx title="src/App.tsx"
import { Refine, WelcomePage } from "@refinedev/core";

function App() {
  return (
    <Refine>
      <WelcomePage />
    </Refine>
  );
}

export default App;
```

Não estamos fazendo nada especial aqui. Estamos apenas montando o componente `<Refine />` no app. O componente `<Refine />` é o componente central do Refine e fornece todo o contexto e a lógica necessários para a aplicação funcionar.

O componente `<WelcomePage />` é fornecido por `@refinedev/core` e exibe uma página simples de boas-vindas ao Refine. Você pode removê-lo se quiser.

Isso basta para colocar nosso app em execução. Agora podemos iniciar a aplicação com o seguinte comando:

```sh
npm run dev
```

Ao abrir o navegador e acessar localhost, você deve ver a página à direita. Se tudo estiver funcionando como esperado, avance para a próxima seção.

</TabItem>

</Tabs>

:::tip Geração de app sob medida

Por padrão, o `create-refine-app` guia você por alguns passos para criar um novo app ajustado às suas necessidades, incluindo data providers, autenticação, UI libraries e mais. Leia mais sobre isso na seção [quickstart](/core/docs/getting-started/quickstart).

:::

</Sandpack>
