---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Implémentez l'i18nProvider de Refine pour traduire les textes, changer de locale et exposer la locale courante."
---

# i18n Provider <GuideBadge id="guides-concepts/i18n" />

Refine utilise `i18nProvider` pour connecter l'application à la bibliothèque de traduction de votre choix.

```ts
import { I18nProvider } from "@refinedev/core";

const i18nProvider: I18nProvider = {
  translate: (key: string, options?: any, defaultMessage?: string) => string,
  changeLocale: (lang: string, options?: any) => Promise,
  getLocale: () => string,
};
```

Après création, passez-le à `<Refine />` :

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import i18nProvider from "./i18nProvider";

const App: React.FC = () => (
  <Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
);
```

## Méthodes

### translate

`translate` reçoit une clé, des options éventuelles et un message par défaut. Elle doit retourner la chaîne affichée.

```ts
function translate(key: string, options?: any, defaultMessage?: string): string;
function translate(key: string, defaultMessage?: string): string;
```

Utilisez ensuite le hook `useTranslation` pour appeler cette méthode depuis vos composants.

### changeLocale

`changeLocale` change la langue active et retourne une `Promise`. La bibliothèque i18n choisie gère le chargement des fichiers et le fallback.

```ts
changeLocale: (locale: string, options?: any) => Promise<any>;
```

### getLocale

`getLocale` retourne la locale actuellement utilisée.

```ts
getLocale: () => string;
```

## Fichiers de traduction

Les composants Refine prennent en charge l'i18n. Vous pouvez fournir vos propres fichiers pour remplacer les textes par défaut, par exemple `public/locales/fr/common.json` avec les libellés de resources, boutons, menus et messages de validation.

## Exemple

<CodeSandboxExample path="i18n-react" />

[use-translation]: /core/docs/i18n/hooks/use-translation
