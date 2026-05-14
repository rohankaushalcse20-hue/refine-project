---
title: Introduction
---

import { Sandpack, AddRouterProviderToApp } from "./sandpack.tsx";

<Sandpack>

Après les bases du data fetching et de l'authentification, cette unité ajoute un router provider à l'application et présente les fonctionnalités débloquées par cette intégration.

Refine propose des intégrations pour les solutions de routing les plus utilisées, comme [React Router](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) et [Remix](/core/docs/routing/integrations/remix).

:::simple Conseils d'implémentation

- Choisissez de préférence une intégration fournie, ou créez votre propre provider avec l'interface router provider de Refine.
- Refine ne remplace pas la façon dont votre router gère les pages ou routes.
- Fournir un router provider active l'inférence de paramètres, la navigation et les redirections sans retirer les fonctionnalités du router.

:::

Cette unité couvre :

- Le concept de resource dans Refine.
- L'inférence de `resource`, `action` et `id` depuis l'URL.
- La navigation et les redirections.
- La synchronisation des états de formulaires et tables avec l'URL.
- La gestion de l'authentification avec les options du router.

## Ajouter le router provider

Nous utiliserons `react-router` pour le routing et `@refinedev/react-router` pour l'intégration avec Refine.

<InstallPackagesCommand args="react-router @refinedev/react-router"/>

Passez ensuite le provider à `<Refine />` et enveloppez l'application avec `<BrowserRouter />`.

```tsx title="src/App.tsx"
import { Refine, Authenticated } from "@refinedev/core";
// highlight-next-line
import routerProvider from "@refinedev/react-router";

// highlight-next-line
import { BrowserRouter } from "react-router";

import { dataProvider } from "./providers/data-provider";
import { authProvider } from "./providers/auth-provider";

export default function App(): JSX.Element {
  return (
    // highlight-next-line
    <BrowserRouter>
      <Refine
        dataProvider={dataProvider}
        authProvider={authProvider}
        // highlight-next-line
        routerProvider={routerProvider}
      >
        <Authenticated key="protected" fallback={<Login />}>
          <Header />
          <ListProducts />
        </Authenticated>
      </Refine>
      {/* highlight-next-line */}
    </BrowserRouter>
  );
}
```

<AddRouterProviderToApp />

Vous êtes maintenant prêt à explorer l'intégration router de Refine.

</Sandpack>
