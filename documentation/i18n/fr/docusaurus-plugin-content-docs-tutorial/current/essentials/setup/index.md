---
title: Votre première application Refine
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

Créer une nouvelle application Refine demande seulement quelques étapes. Pour ce tutoriel, nous n'utiliserons pas tout le potentiel de `create-refine-app` : nous partirons d'une application vide, installerons les dépendances nécessaires et configurerons Refine manuellement.

<Tabs wrapContent={false}>

<TabItem value="quick" label="Quick Setup">

Pour suivre le tutoriel rapidement, utilisez le starter fourni par `create-refine-app`. La commande suivante crée un projet vide avec `@refinedev/core` et `@refinedev/cli`.

```sh
npm create refine-app@latest -- --example starter-vite
```

</TabItem>

<TabItem value="manual" label="Manual Setup">

Créez d'abord l'application avec le template Vite adapté.

```sh
npm create vite@latest my-refine-app -- --template react-ts
```

Installez ensuite les dépendances Refine.

```sh
npm install @refinedev/core @refinedev/cli
```

### Configurer les scripts

Remplacez les scripts `dev`, `build` et `serve` par :

```json
{
  "scripts": {
    "dev": "refine dev",
    "build": "refine build",
    "serve": "refine serve"
  }
}
```

Les commandes `refine` utilisent les commandes du bundler tout en ajoutant des vérifications de versions et des annonces utiles.

### Configurer l'application

Montez `<Refine />` à la racine de l'application.

```tsx title="src/App.tsx"
import { Refine, WelcomePage } from "@refinedev/core";

function App() {
  return (
    <Refine>
      <WelcomePage />
    </Refine>
  );
}

export default App;
```

Lancez ensuite l'application :

```sh
npm run dev
```

Lorsque la page s'affiche correctement dans le navigateur, passez à la section suivante.

</TabItem>

</Tabs>

:::tip Génération adaptée

`create-refine-app` peut configurer data providers, authentification, bibliothèques UI et autres choix dès la création. Consultez le [démarrage rapide](/core/docs/getting-started/quickstart) pour plus de détails.

:::

</Sandpack>
