---
title: "Tabelas e listas | Refine v5"
display_title: "Tabelas"
sidebar_label: "Tabelas"
description: "Crie tabelas, listas, filtros, ordenação e paginação com Refine."
---

Tabelas e listas tornam os dados da API úteis na interface. O Refine fornece hooks que conectam paginação, filtros, ordenação e loading ao data provider.

## Listagens

`useTable` e `useList` são a base para telas de listagem com integrações de UI ou componentes próprios.

```tsx
const table = useTable({
  resource: "products",
  pagination: { pageSize: 10 },
});
```

## Filtros e ordenação

Filtros e sorters são convertidos em parâmetros que o data provider encaminha para a API. Isso mantém a comunicação com o backend desacoplada da UI.

## Ações de CRUD

As listagens podem ser conectadas diretamente a ações de Create, Edit, Show e Delete. Nesse fluxo, é possível respeitar permissões e labels traduzidos com i18n.
