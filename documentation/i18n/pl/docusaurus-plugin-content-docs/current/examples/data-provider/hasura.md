---
id: hasura
title: "Przykład Hasura | Integracja REST API w Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Wdróż Hasura w Refine v5. Poznaj kluczowe kroki i skalowanie REST oraz GraphQL dla własnych API i skalowalnych przepływów danych. Zawiera praktyczne przykłady."
example-tags: [data-provider, live-provider]
---

Z Refine może współpracować dowolny własny backend REST lub GraphQL. Refine [Hasura](https://hasura.io/) GraphQL Data Provider jest dostępny od razu. Dzięki Refine możesz połączyć się z bazą Hasura, tworzyć specjalne zapytania i łatwo korzystać z danych. Ten przykład szczegółowo pokazuje, jak używać danych z bazy Hasura w projekcie Refine.

## Typ danych ID

Domyślnie data provider zakłada, że typ `ID` to `uuid`. Możesz zmienić to zachowanie za pomocą opcji `idType`. Jako wartość `idType` możesz przekazać `Int` albo `uuid`, albo użyć funkcji, która określi `idType` na podstawie nazwy zasobu.

#### Przekazanie 'Int' albo 'uuid' do `idType`

Pozwoli to ustawić `idType` dla wszystkich zasobów.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### Przekazanie funkcji do `idType`

Pozwoli to określać `idType` na podstawie nazwy zasobu.

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
