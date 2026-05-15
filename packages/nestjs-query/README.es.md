# Data provider NestJS Query para Refine

`@refinedev/nestjs-query` conecta Refine con APIs basadas en [NestJS Query](https://doug-martin.github.io/nestjs-query/). Incluye data provider y live provider para trabajar con GraphQL y suscripciones.

## Instalacion

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## Uso basico

```tsx
import dataProvider, { GraphQLClient, liveProvider } from "@refinedev/nestjs-query";
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

## Documentacion

Consulta la [documentacion de data providers de Refine](https://refine.dev/docs/data/data-provider/) y la referencia de NestJS Query para adaptar recursos, filtros y relaciones.
