---
title: Einen Datensatz aktualisieren
---

import { Sandpack, AddUpdateMethod, CreateEditProductFile, AddUseUpdateToEditProduct, AddEditProductToAppTsx } from "./sandpack.tsx";

<Sandpack>

In diesem Schritt lernst du Refines Hook `useUpdate` kennen, um einen Datensatz in unserer API zu aktualisieren und die Methode `update` in unserem Data Provider zu implementieren.

## Die Methode `update` implementieren

Damit wir mit Refines Hooks einen Datensatz aktualisieren koennen, muessen wir zuerst die Methode [`update`](/core/docs/data/data-provider/#update-) in unserem Data Provider implementieren. Diese Methode wird aufgerufen, wenn wir den Hook [`useUpdate`](/core/docs/data/hooks/use-update) oder seine Erweiterungen in unseren Komponenten verwenden.

Die Methode `update` akzeptiert die Eigenschaften `resource`, `id`, `variables` und `meta`.

- `resource` bezeichnet die Entitaet, die wir aktualisieren.
- `id` ist die ID des Datensatzes, den wir aktualisieren.
- `variables` ist ein Objekt mit den Daten, die wir an die API senden.
- `meta` ist ein Objekt mit zusaetzlichen Daten, die an den Hook uebergeben wurden.

Die Entitaet `products` unserer Fake-API erwartet, dass wir einen Datensatz ueber den Endpoint `/products/:id` mit einem `PATCH`-Request aktualisieren. Deshalb verwenden wir die Eigenschaften `resource`, `id` und `variables`, um den Request zu erstellen.

Aktualisiere deine Datei `src/providers/data-provider.ts`, indem du die folgenden Zeilen hinzufuegst:

```ts title="src/providers/data-provider.ts"
import type { DataProvider } from "@refinedev/core";

const API_URL = "https://api.fake-rest.refine.dev";

export const dataProvider: DataProvider = {
  getOne: async ({ resource, id, meta }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`);

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-start
  update: async ({ resource, id, variables }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`, {
      method: "PATCH",
      body: JSON.stringify(variables),
      headers: {
        "Content-Type": "application/json",
      },
    });

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-end
  getList: () => {
    throw new Error("Not implemented");
  },
  /* ... */
};
```

<AddUpdateMethod />

## Den Hook `useUpdate` verwenden

Nachdem wir die Methode `update` implementiert haben, koennen wir den Hook `useUpdate` aufrufen und einen einzelnen Datensatz in unserer API aktualisieren. Erstellen wir eine Komponente namens `EditProduct` und mounten sie innerhalb unserer Komponente `<Refine />`.

<CreateEditProductFile />

Zunaechst fuegen wir in unserer Komponente `EditProduct` einen Aufruf des Hooks `useOne` ein, um den Datensatz abzurufen, den wir aktualisieren moechten.

Danach verwenden wir den Hook `useUpdate` innerhalb von `EditProduct`, um einen einzelnen Datensatz der Entitaet `products` in unserer API zu aktualisieren.

Aktualisiere deine Datei `src/pages/products/edit.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/pages/products/edit.tsx"
// highlight-next-line
import { useOne, useUpdate } from "@refinedev/core";

export const EditProduct = () => {
  const {
    result,
    query: { isLoading },
  } = useOne({ resource: "products", id: 123 });
  // highlight-next-line
  const {
    mutate,
    mutation: { isPending: isUpdating },
  } = useUpdate();

  if (isLoading) {
    return <div>Loading...</div>;
  }

  const updatePrice = async () => {
    // highlight-start
    await mutate({
      resource: "products",
      id: 123,
      values: {
        price: Math.floor(Math.random() * 100),
      },
    });
    // highlight-end
  };

  return (
    <div>
      <div>Product name: {result?.name}</div>
      <div>Product price: ${result?.price}</div>
      <button onClick={updatePrice}>Update Price</button>
    </div>
  );
};
```

<AddUseUpdateToEditProduct />

Zum Schluss mounten wir unsere Komponente `EditProduct` innerhalb der Komponente `<Refine />`.

Aktualisiere deine Datei `src/App.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";

import { ShowProduct } from "./pages/products/show";
// highlight-next-line
import { EditProduct } from "./pages/products/edit";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider}>
      {/* <ShowProduct /> */}
      {/* highlight-next-line */}
      <EditProduct />
    </Refine>
  );
}
```

<AddEditProductToAppTsx />

Jetzt solltest du sowohl den Produktnamen als auch den Preis auf dem Bildschirm sehen koennen. Sobald du auf die Schaltflaeche `Update Price` klickst, wird der Preis des Produkts aktualisiert.

:::tip Intelligente Invalidierungen

Wenn wir den Preis mit `useUpdate` aktualisieren, wird der zuvor aufgerufene Hook `useOne` automatisch invalidiert. Das liegt daran, dass Refine alle Queries invalidiert, die dieselbe Resource und dieselbe ID verwenden, wenn ein Datensatz aktualisiert wird. So stellen wir sicher, dass auf dem Bildschirm immer die aktuellen Daten angezeigt werden und wir die Queries nicht manuell invalidieren muessen.

:::

Im naechsten Schritt lernst du Refines Hook `useList` kennen, um eine Liste von Datensaetzen aus unserer API abzurufen und die Methode `getList` in unserem Data Provider zu implementieren.

</Sandpack>
