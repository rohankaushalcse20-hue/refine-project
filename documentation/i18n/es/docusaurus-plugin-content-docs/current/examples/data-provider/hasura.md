---
id: hasura
title: "Ejemplo de Hasura | Integración REST API en Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Aprende a usar Hasura con Refine v5 y a ajustar el tipo de ID según tus resources."
example-tags: [data-provider, live-provider]
---

Cualquier backend personalizado en REST o GraphQL puede integrarse con Refine. El GraphQL Data Provider de [Hasura](https://hasura.io/) viene listo para usar con Refine. Gracias a ello puedes conectarte a tu base de datos de Hasura, crear consultas específicas y trabajar con tus datos de forma sencilla. Este ejemplo muestra en detalle cómo usar los datos de Hasura dentro de un proyecto Refine.

## Tipo de dato para ID

Por defecto, el data provider asume que el tipo `ID` es `uuid`. Puedes cambiar este comportamiento usando la opción `idType`. Puedes pasar `Int` o `uuid` como valor de `idType`, o bien usar una función para decidir el tipo según el nombre del resource.

#### Pasar `'Int'` o `'uuid'` a `idType`

Esto te permite definir el `idType` para todos los resources.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### Pasar una función a `idType`

Esto te permite definir el `idType` en función del nombre del resource.

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
