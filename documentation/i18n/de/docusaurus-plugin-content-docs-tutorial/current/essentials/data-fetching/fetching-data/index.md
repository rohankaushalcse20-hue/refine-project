---
title: Einen Datensatz abrufen
---

import { Sandpack, AddGetOneMethod, CreateShowProductFile, AddUseOneToShowProduct, AddShowProductToAppTsx } from "./sandpack.tsx";

<Sandpack>

In diesem Schritt lernst du Refines Hook `useOne` kennen, um einen einzelnen Datensatz aus unserer API abzurufen und die Methode `getOne` in unserem Data Provider zu implementieren.

## Die Methode `getOne` implementieren

Damit wir mit Refines Hooks einen Datensatz abrufen koennen, muessen wir zuerst die Methode [`getOne`](/core/docs/data/data-provider/#getone-) in unserem Data Provider implementieren. Diese Methode wird aufgerufen, wenn wir den Hook [`useOne`](/core/docs/data/hooks/use-one) oder seine Erweiterungen in unseren Komponenten verwenden.

Die Methode `getOne` akzeptiert die Eigenschaften `resource`, `id` und `meta`.

- `resource` bezeichnet die Entitaet, die wir abrufen.
- `id` ist die ID des Datensatzes, den wir abrufen.
- `meta` ist ein Objekt mit zusaetzlichen Daten, die an den Hook uebergeben wurden.

Unsere Fake-API hat die Entitaet `products` und erwartet, dass wir einen einzelnen Datensatz ueber den Endpoint `/products/:id` abrufen. Deshalb verwenden wir die Eigenschaften `resource` und `id`, um den Request zu erstellen.

Aktualisiere deine Datei `src/providers/data-provider.ts`, indem du die folgenden Zeilen hinzufuegst:

```ts title="src/providers/data-provider.ts"
import type { DataProvider } from "@refinedev/core";

const API_URL = "https://api.fake-rest.refine.dev";

export const dataProvider: DataProvider = {
  // highlight-start
  getOne: async ({ resource, id, meta }) => {
    const response = await fetch(`${API_URL}/${resource}/${id}`);

    if (response.status < 200 || response.status > 299) throw response;

    const data = await response.json();

    return { data };
  },
  // highlight-end
  update: () => {
    throw new Error("Not implemented");
  },
  getList: () => {
    throw new Error("Not implemented");
  },
  /* ... */
};
```

<AddGetOneMethod />

## Den Hook `useOne` verwenden

Nachdem wir die Methode `getOne` implementiert haben, koennen wir den Hook `useOne` aufrufen und einen einzelnen Datensatz aus unserer API abrufen. Erstellen wir eine Komponente namens `ShowProduct` und mounten sie innerhalb unserer Komponente `<Refine />`.

<CreateShowProductFile />

Danach importieren wir den Hook `useOne` und verwenden ihn in unserer Komponente `ShowProduct`, um einen einzelnen Datensatz der Entitaet `products` aus unserer API abzurufen.

Aktualisiere deine Datei `src/pages/products/show.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/pages/products/show.tsx"
// highlight-next-line
import { useOne } from "@refinedev/core";

export const ShowProduct = () => {
  // highlight-next-line
  const {
    result,
    query: { isLoading },
  } = useOne({ resource: "products", id: 123 });

  if (isLoading) {
    return <div>Loading...</div>;
  }

  return <div>Product name: {result?.name}</div>;
};
```

<AddUseOneToShowProduct />

Zum Schluss mounten wir die Komponente `ShowProduct` innerhalb unserer Komponente `<Refine />`.

Aktualisiere deine Datei `src/App.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import { dataProvider } from "./providers/data-provider";
// highlight-next-line
import { ShowProduct } from "./pages/products/show";

export default function App(): JSX.Element {
  return (
    <Refine dataProvider={dataProvider}>
      {/* highlight-next-line */}
      <ShowProduct />
    </Refine>
  );
}
```

<AddShowProductToAppTsx />

Jetzt solltest du den Produktnamen auf dem Bildschirm sehen koennen.

Im naechsten Schritt lernst du Refines Hook `useUpdate` kennen, um einen einzelnen Datensatz in unserer API zu aktualisieren und die Methode `update` in unserem Data Provider zu implementieren.

</Sandpack>
