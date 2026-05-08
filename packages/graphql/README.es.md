# Data provider GraphQL

`@refinedev/graphql` ofrece un data provider para conectar proyectos Refine con backends GraphQL personalizados. Sirve como base flexible cuando quieres definir tus propios queries, mutations y convenciones de transporte.

## Instalación

```sh
npm install @refinedev/graphql
```

## Uso básico

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => {
  return (
    <Refine dataProvider={dataProvider(client)}>
      {/* ... */}
    </Refine>
  );
};
```

## Cuándo usarlo

Úsalo cuando tu backend exponga un endpoint GraphQL y necesites adaptar la capa de datos de Refine a tus tipos, resources y convenciones de consulta.

## Más información

Consulta la documentación del data provider GraphQL de Refine para ampliar la integración.
