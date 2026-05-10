---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Configure o routing do Refine com React Router, Next.js, Remix ou outro sistema compatível."
---

O roteamento é essencial em qualquer aplicação CRUD. A arquitetura headless do Refine permite escolher o roteador sem ficar preso a um framework específico.

O Refine oferece integrações prontas para **React Router**, **Next.js** e **Remix**. Elas ajudam a reconhecer parâmetros automaticamente, tratar redirecionamentos após mutações ou login e reutilizar utilitários de navegação de forma consistente.

Mesmo assim, o Refine continua agnóstico em relação ao roteador. Você define as rotas: com `Routes` no React Router, com `pages` ou `app` no Next.js e com `app/routes` no Remix.

## Conectando o router provider

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Routes } from "react-router";

export const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* suas rotas */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

Mantenha rotas e resources alinhados para que o Refine consiga derivar `resource`, `id` e outros parâmetros diretamente da URL.
