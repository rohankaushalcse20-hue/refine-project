---
id: hasura
title: "Hasura-Beispiel | REST-API-Integration in Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Implementiere Hasura in Refine v5. Lerne skalierbare REST- und GraphQL-Muster fuer eigene APIs und Datenfluesse mit praktischen Beispielen."
example-tags: [data-provider, live-provider]
---

Jedes eigene REST- oder GraphQL-Backend kann mit Refine integriert werden. Der Refine [Hasura](https://hasura.io/) GraphQL Data Provider ist sofort einsatzbereit. Dank Refine kannst du dich mit deiner Hasura-Datenbank verbinden, spezielle Abfragen erstellen und deine Daten einfach verwenden. Dieses Beispiel zeigt im Detail, wie du Daten aus deiner Hasura-Datenbank mit einem Refine-Projekt nutzt.

## ID Data Type

Standardmaessig nimmt der Data Provider an, dass dein `ID`-Typ `uuid` ist. Du kannst dieses Verhalten mit der Option `idType` aendern. Du kannst `Int` oder `uuid` als Wert fuer `idType` uebergeben oder eine Funktion verwenden, um `idType` anhand des Ressourcennamens zu bestimmen.

#### Passing 'Int' or 'uuid' to `idType`

Damit kannst du `idType` fuer alle Ressourcen bestimmen.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### Passing function to `idType`

Damit kannst du `idType` anhand des Ressourcennamens bestimmen.

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
