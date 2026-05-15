# Integracao Hasura para refine

`@refinedev/hasura` conecta aplicacoes refine ao [Hasura](https://hasura.io/) por GraphQL. Use este pacote quando o Hasura gerar a API sobre seus dados e o refine for responsavel pelas telas CRUD.

## Instalacao

```sh
npm install @refinedev/hasura
```

## Uso basico

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("HASURA_API_URL", {
  headers: {
    "x-hasura-role": "public",
  },
});

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

## Documentacao

- Consulte a [documentacao de data provider do refine](https://refine.dev/docs/core/providers/data-provider).
- Veja os [tutoriais do refine](https://refine.dev/docs/tutorial/introduction/index/).
