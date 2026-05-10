---
title: "Conceitos gerais | Refine v5"
display_title: "Conceitos gerais"
sidebar_label: "Conceitos gerais"
description: "Entenda a arquitetura headless, resources, providers, hooks e meta no Refine."
---

O Refine é um framework extensível para criar aplicações web rapidamente. Sua arquitetura combina **hooks**, **providers** conectáveis e uma camada confiável de dados e estado.

## Conceito headless

O Refine não prende sua aplicação a um conjunto fixo de componentes visuais. Ele fornece `hooks`, `components`, `providers` e utilitários, enquanto mantém a lógica de negócio separada da apresentação.

Isso permite trabalhar com design systems próprios, Tailwind CSS, Ant Design, Material UI, Mantine ou Chakra UI sem abrir mão das vantagens de `@refinedev/core`.

## Resources

Um **resource** representa uma entidade da aplicação, como `products`, `blogPosts` ou `orders`. Resources conectam rotas, ações de CRUD, menus e providers dentro de uma estrutura previsível.

## Providers

Providers lidam com acesso a dados, autenticação, autorização, notificações, i18n, tempo real, roteamento e audit logs. Você pode usar implementações prontas ou criar as suas.

## Hooks

Os hooks do Refine são headless e independentes da biblioteca de UI. APIs como `useGo`, `useCan` e `useTranslate` oferecem uma interface única para navegação, permissões e tradução.

## Meta

A propriedade `meta` permite enviar informações extras para providers e hooks, como headers, parâmetros especiais, seleção de campos, contexto de multi-tenant ou consultas GraphQL.
