---
title: "Internationalisation (i18n) | Refine v5"
display_title: "Internationalisation (i18n)"
sidebar_label: "Internationalisation (i18n)"
description: "Localisez les applications Refine avec un i18nProvider, des fichiers de traduction et des hooks dédiés."
---

L'internationalisation permet d'adapter une application à plusieurs langues et régions. Refine peut fonctionner avec n'importe quelle bibliothèque i18n à condition de fournir un `i18nProvider`.

## i18nProvider

Le provider centralise trois opérations : traduire une clé, changer de locale et connaître la locale courante.

```ts
import { I18nProvider } from "@refinedev/core";

const i18nProvider: I18nProvider = {
  translate: (key: string, options?: any, defaultMessage?: string) => string,
  changeLocale: (lang: string, options?: any) => Promise,
  getLocale: () => string,
};
```

Passez ensuite ce provider à `<Refine />` :

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import i18nProvider from "./i18nProvider";

const App = () => (
  <Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
);
```

## Bibliothèques compatibles

Vous pouvez utiliser `react-i18next`, FormatJS, Lingui ou une solution interne. Refine se limite à l'interface du provider et laisse la bibliothèque gérer les fichiers, namespaces, fallback et détection de langue.

## Traduire l'interface CRUD

Les composants Refine lisent les clés de traduction via `useTranslation`. Vous pouvez localiser les menus, boutons, titres de resources, messages de validation, notifications et champs visibles.

## Changer de locale

Un sélecteur de langue peut appeler `changeLocale`. Les pages qui utilisent les hooks de traduction se mettent alors à jour selon la bibliothèque i18n choisie.

## À préserver

Ne traduisez pas les noms de packages, commandes, imports, props, routes techniques et identifiants d'API. Localisez uniquement les libellés et explications destinés aux utilisateurs.
