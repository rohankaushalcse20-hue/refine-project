---
title: Data Fetching
---

import { Sandpack, FocusOnDataProviderFile, AddDataProviderToRefine } from "./sandpack.tsx";

<Sandpack>

In diesem Schritt lernst du die Grundlagen des Data Fetching in Refine kennen. Die Komponente `<Refine />` akzeptiert eine [`dataProvider`](/core/docs/core/refine-component/#dataprovider-)-Prop, die alle Data-Fetching- und Mutationsvorgaenge ueber eine einfache Schnittstelle abwickelt. Refine unterstuetzt viele Data Provider direkt, aber fuer dieses Tutorial erstellen wir unseren eigenen Data Provider und verbinden ihn mit einer [Fake-REST-API](https://api.fake-rest.refine.dev/).

Mehr ueber die unterstuetzten Data Provider findest du im Abschnitt [Supported Data Providers](/core/docs/guides-concepts/data-fetching/#supported-data-providers) des Data-Fetching-Leitfadens.

## Einen Data Provider erstellen

Wir implementieren jede Methode einzeln, damit alle Details nachvollziehbar bleiben. Fuer API-Requests verwenden wir `fetch`; du kannst aber jede Bibliothek einsetzen, die dir passt.

Zuerst erstellen wir in unserem Projekt die Datei `src/providers/data-provider.ts`. Sie enthaelt alle Methoden, die wir fuer unseren Data Provider implementieren muessen.

Um einen leeren Data Provider zu sehen, <FocusOnDataProviderFile>oeffne `src/providers/data-provider.ts`</FocusOnDataProviderFile> im rechten Panel.

Danach uebergeben wir unseren Data Provider in der Datei `src/App.tsx` ueber die Prop `dataProvider` an die Komponente `<Refine />`.

Aktualisiere deine Datei `src/App.tsx`, indem du die folgenden Zeilen hinzufuegst:

```tsx
import { Refine, WelcomePage } from "@refinedev/core";

// highlight-next-line
import { dataProvider } from "./providers/data-provider";

export default function App(): JSX.Element {
  return (
    // highlight-next-line
    <Refine dataProvider={dataProvider}>
      <WelcomePage />
    </Refine>
  );
}
```

<AddDataProviderToRefine />

:::tip

Mit Refine kannst du auch mehrere Data Provider verwenden. Mehr dazu findest du im Abschnitt [Multiple Data Providers](/core/docs/guides-concepts/data-fetching/#multiple-data-providers) des Data-Fetching-Leitfadens.

:::

Im naechsten Schritt lernst du, mit Refines Hook `useOne` einen Datensatz abzurufen und die Methode `getOne` in unserem Data Provider zu implementieren.

</Sandpack>
