# Integracao GraphQL para refine

`@refinedev/graphql` fornece um data provider para APIs [GraphQL](https://graphql.org/). Ele conecta o contrato de dados do refine a um `GraphQLClient`, mantendo listas, detalhes, criacao, edicao e exclusao dentro do fluxo CRUD do framework.

## Instalacao

```sh
npm install @refinedev/graphql
```

## Uso basico

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

## Documentacao

- Consulte a [documentacao de data provider do refine](https://refine.dev/docs/core/providers/data-provider).
- Leia a [documentacao GraphQL do refine](https://refine.dev/docs/packages/documentation/data-providers/graphql/).
