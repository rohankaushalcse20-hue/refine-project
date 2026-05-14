---
title: Introdução
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

Este tutorial conduz você dos fundamentos do Refine até tópicos mais avançados. Você vai aprender a criar uma aplicação CRUD completa com Refine.

O Refine não depende de um roteador específico, então você pode escolher a biblioteca de routing com a qual tem mais familiaridade. O Refine oferece suporte oficial a [React Router DOM](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) e [Remix](/core/docs/routing/integrations/remix). Nas próximas etapas do tutorial, o conteúdo exibido será ajustado de acordo com a sua seleção de routing. Você pode alterar essa seleção a qualquer momento para ver o conteúdo das outras bibliotecas.

Escolha a biblioteca de routing com a qual deseja continuar:

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

Nas próximas unidades deste tutorial, você também escolherá uma integração de UI framework do Refine e aprenderá como essas integrações são feitas e em que situações são úteis. Embora o Refine ofereça suporte oficial a Ant Design, Material UI, Mantine e Chakra UI, este tutorial foi preparado para os dois frameworks de UI mais usados: [Ant Design](/core/docs/ui-integrations/ant-design/introduction) e [Material UI](/core/docs/ui-integrations/material-ui/introduction).

Escolha o UI framework com o qual deseja continuar:

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

Você encontra o material correspondente para outros UI frameworks na [documentação](/core/docs/guides-concepts/ui-libraries).

## Conteúdo do tutorial

Abaixo estão todas as seções do tutorial organizadas por tema:

### Fundamentos

- [Seu primeiro app Refine](/core/tutorial/essentials/setup/)
- [Buscando um registro](/core/tutorial/essentials/data-fetching/fetching-data/)
- [Atualizando um registro](/core/tutorial/essentials/data-fetching/updating-data/)
- [Listando registros](/core/tutorial/essentials/data-fetching/listing-data/)
- [Formulários](/core/tutorial/essentials/forms/)
- [Tabelas](/core/tutorial/essentials/tables/)

### Autenticação

- [Introdução](/core/tutorial/authentication/intro/)
- [Protegendo conteúdo](/core/tutorial/authentication/protecting-content/)
- [Login e logout](/core/tutorial/authentication/logging-in-out/)
- [Usando a identidade do usuário](/core/tutorial/authentication/user-identity/)
- [Integração com data provider](/core/tutorial/authentication/data-provider-integration/)

### Routing com React Router

- [Introdução](/core/tutorial/routing/intro/react-router/)
- [Autenticação](/core/tutorial/routing/authentication/react-router/)
- [Definindo resources](/core/tutorial/routing/resource-definition/react-router/)
- [Navegação](/core/tutorial/routing/navigation/react-router/)
- [Inferindo parâmetros](/core/tutorial/routing/inferring-parameters/react-router/)
- [Redirecionamentos](/core/tutorial/routing/redirects/react-router/)
- [Sincronizando estado com a location](/core/tutorial/routing/syncing-state/react-router/)

### UI Libraries com Ant Design

- [Introdução](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [Usando layouts](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [Refatoração](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [Componentes CRUD](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [Notificações](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [Autenticação](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### UI Libraries com Material UI

- [Introdução](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [Usando layouts](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [Refatoração](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [Componentes CRUD](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [Notificações](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [Autenticação](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### Próximos passos com Ant Design

- [Introdução](/core/tutorial/next-steps/intro/ant-design/)
- [Usando o Inferencer](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [Usando a CLI](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [Usando o Devtools](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [Resumo](/core/tutorial/next-steps/summary/react-router/ant-design/)

### Próximos passos com Material UI

- [Introdução](/core/tutorial/next-steps/intro/material-ui/)
- [Usando o Inferencer](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [Usando a CLI](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [Usando o Devtools](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [Resumo](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
