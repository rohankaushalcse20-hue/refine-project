---
title: "I18n Provider | Refine v5"
display_title: "I18n Provider"
sidebar_label: "I18n Provider"
description: "Connectez Refine à votre bibliothèque de traduction préférée avec i18nProvider."
---

Refine n'impose pas de bibliothèque de traduction. Il utilise un `i18nProvider` qui adapte `react-i18next`, `next-i18next` ou une solution interne.

## Interface minimale

```tsx
const i18nProvider = {
  translate: (key, options, defaultMessage) => defaultMessage ?? key,
  changeLocale: (lang) => Promise.resolve(lang),
  getLocale: () => "fr",
};
```

Passez ce provider à `<Refine />` pour que hooks, menus, boutons et composants accèdent aux traductions.

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

Utilisez `useTranslate`, `useSetLocale` et `useGetLocale` pour traduire, changer de langue et lire la locale active.
