---
title: Data fetching
---

import { Sandpack, FocusOnDataProviderFile, AddDataProviderToRefine } from "./sandpack.tsx";

<Sandpack>

Dans cette étape, vous découvrirez les bases du data fetching dans Refine. Le composant `<Refine />` accepte une prop [`dataProvider`](/core/docs/core/refine-component/#dataprovider-) qui gère les opérations de lecture et mutation à travers une interface simple.

Refine fournit plusieurs data providers prêts à l'emploi. Pour ce tutoriel, nous créerons le nôtre et le connecterons à une [fake REST API](https://api.fake-rest.refine.dev/).

## Créer un data provider

Nous implémenterons les méthodes une par une. Les requêtes utiliseront `fetch`, mais vous pouvez choisir une autre bibliothèque.

Créez d'abord `src/providers/data-provider.ts`, qui contiendra les méthodes du provider. Pour voir un provider vide, <FocusOnDataProviderFile>ouvrez `src/providers/data-provider.ts`</FocusOnDataProviderFile> dans le panneau de droite.

Ajoutez ensuite le provider à `<Refine />` dans `src/App.tsx` :

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

Refine peut aussi utiliser plusieurs data providers dans une même application. Consultez la section [Multiple Data Providers](/core/docs/guides-concepts/data-fetching/#multiple-data-providers) du guide Data Fetching.

:::

Dans l'étape suivante, vous récupérerez un enregistrement avec le hook `useOne` et implémenterez la méthode `getOne`.

</Sandpack>
