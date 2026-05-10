---
title: "Data Fetching | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "Aprenda como o Refine conecta a UI às APIs usando data providers e hooks."
---

Os dados estão no centro de quase toda aplicação administrativa. O Refine conecta a UI a uma ou mais fontes de dados por meio de um `dataProvider`, que implementa a interface [`DataProvider`](/core/docs/core/interface-references#dataprovider).

O data provider recebe informações como `resource`, `id` e `meta` e decide qual endpoint ou query deve ser usado para acessar a fonte real.

## Hooks de dados

Depois que o provider é registrado, você pode executar operações de CRUD com hooks como `useList`, `useOne`, `useCreate`, `useUpdate` e `useDelete`.

```tsx
import { useOne } from "@refinedev/core";

const Product = () => {
  const { data, isLoading } = useOne({ resource: "products", id: 1 });
  if (isLoading) return <span>Loading...</span>;
  return <pre>{JSON.stringify(data, null, 2)}</pre>;
};
```

## Estado e cache

Os data hooks usam TanStack Query para lidar com loading, erros, cache, deduplicação de requests, invalidação e atualizações otimistas.

## Vários providers

Você pode usar REST para um resource e GraphQL para outro sem mudar a API usada nos componentes.
