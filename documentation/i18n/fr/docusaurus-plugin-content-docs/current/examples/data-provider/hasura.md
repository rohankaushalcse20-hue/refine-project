---
id: hasura
title: "Exemple Hasura | Intégration d'API REST dans Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Implémentez Hasura dans Refine v5. Découvrez les étapes clés pour faire évoluer REST et GraphQL avec des APIs personnalisées et des flux de données maintenables."
example-tags: [data-provider, live-provider]
---

Tout backend personnalisé REST ou GraphQL peut être intégré avec Refine. Le GraphQL Data Provider [Hasura](https://hasura.io/) de Refine est disponible prêt à l'emploi. Grâce à Refine, vous pouvez vous connecter à votre base Hasura, créer des requêtes spécifiques et utiliser facilement vos données. Cet exemple montre en détail comment exploiter les données de votre base Hasura dans un projet Refine.

## Type de données ID

Par défaut, le data provider suppose que votre type `ID` est `uuid`. Vous pouvez changer ce comportement avec l'option `idType`. Vous pouvez passer `Int` ou `uuid` comme valeur de l'option `idType`, ou utiliser une fonction pour déterminer `idType` selon le nom de la resource.

#### Passer 'Int' ou 'uuid' à `idType`

Cela vous permet de déterminer `idType` pour toutes les resources.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### Passer une fonction à `idType`

Cela vous permet de déterminer `idType` selon le nom de la resource.

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
