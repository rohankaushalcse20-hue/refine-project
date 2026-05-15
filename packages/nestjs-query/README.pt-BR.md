# Integracao NestJS Query para refine

`@refinedev/nestjs-query` conecta o refine a APIs criadas com [NestJS Query](https://doug-martin.github.io/nestjs-query/docs). Ele fornece data provider GraphQL e suporte a eventos em tempo real via `graphql-ws`.

## Instalacao

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## Uso basico

```tsx
import dataProvider, {
  GraphQLClient,
  liveProvider,
} from "@refinedev/nestjs-query";
import { createClient } from "graphql-ws";

const App = () => (
  <Refine
    dataProvider={dataProvider(new GraphQLClient("API_URL"))}
    liveProvider={liveProvider(createClient({ url: "WS_URL" }))}
  >
    {/* ... */}
  </Refine>
);
```

## Documentacao

- Consulte a [documentacao de data provider do refine](https://refine.dev/docs/core/providers/data-provider).
- Veja o [exemplo NestJS Query do refine](https://refine.dev/docs/examples/data-provider/nestjs-query/).
