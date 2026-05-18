---
id: hasura
title: "Exemplo Hasura | Integração REST API no Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Implemente Hasura no Refine v5. Aprenda as etapas principais para escalar REST e GraphQL em APIs customizadas e fluxos de dados."
example-tags: [data-provider, live-provider]
---

Qualquer backend customizado REST ou GraphQL pode ser integrado ao Refine. O [Hasura](https://hasura.io/) GraphQL Data Provider do Refine vem pronto para uso. Com o Refine, você pode conectar seu banco de dados Hasura, criar consultas especiais e usar seus dados com facilidade. Este exemplo mostra em detalhes como usar os dados do seu banco Hasura em um projeto Refine.

## Tipo de dado de ID

Por padrão, o data provider presume que o tipo de `ID` é `uuid`; você pode alterar esse comportamento usando a opção `idType`. É possível passar `Int` ou `uuid` como valor da opção `idType`, ou usar uma função para determinar o `idType` com base no nome do recurso.

#### Passando 'Int' ou 'uuid' para `idType`

Isso permite determinar o `idType` para todos os recursos.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### Passando uma função para `idType`

Isso permite determinar o `idType` com base no nome do recurso.

```tsx
const idTypeMap: Record<string, "Int" | "uuid"> = {
  users: "Int",
  posts: "uuid",
};

const myDataProvider = dataProvider(client, {
  idType: (resource) => idTypeMap[resource] ?? "uuid",
});
```

<CodeSandboxExample path="data-provider-hasura" />
