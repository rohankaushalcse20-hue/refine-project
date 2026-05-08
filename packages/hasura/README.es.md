# Integración Hasura

`@refinedev/hasura` conecta Refine con proyectos Hasura y simplifica el consumo de GraphQL en aplicaciones CRUD. Es una buena opción cuando quieres trabajar con queries, mutations y suscripciones desde una base alineada con el ecosistema Hasura.

## Instalación

```sh
npm install @refinedev/hasura
```

## Uso básico

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("HASURA_API_URL", {
  headers: {
    "x-hasura-role": "public",
  },
});

const App = () => {
  return (
    <Refine dataProvider={dataProvider(client)}>
      {/* ... */}
    </Refine>
  );
};
```

## Cuándo usarlo

Úsalo cuando tu proyecto dependa de Hasura para exponer GraphQL, gestionar roles o añadir capacidades realtime con una integración ya preparada.

## Más información

Revisa la documentación de Refine para data providers y la guía específica de Hasura para adaptar la integración a tu esquema.
