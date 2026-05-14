---
title: "Notifications | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "Centralisez les messages de succès, d'erreur et d'information avec le notificationProvider de Refine."
---

Les notifications informent l'utilisateur qu'une action a réussi, échoué ou nécessite son attention. Refine les centralise avec `notificationProvider`.

## Notification provider

Le provider expose des méthodes comme `open` et `close`. Vous pouvez l'adapter à React Toastify, Ant Design, Material UI ou à votre propre système de notifications.

```tsx
const notificationProvider = {
  open: ({ key, message, description, type }) => {
    notify({ key, message, description, type });
  },
  close: (key) => {
    dismiss(key);
  },
};
```

Passez-le à `<Refine />` pour que les hooks et composants puissent l'utiliser.

## Notifications automatiques

Les mutations peuvent afficher automatiquement des messages de succès ou d'erreur. Vous pouvez garder les messages par défaut ou fournir `successNotification` et `errorNotification` dans les hooks.

```tsx
useUpdate({
  resource: "products",
  successNotification: () => ({
    message: "Product updated",
    type: "success",
  }),
});
```

## Hook useNotification

`useNotification` donne accès au provider depuis vos composants. Utilisez-le pour les messages qui ne viennent pas directement d'une mutation Refine.

## i18n

Dans une application multilingue, traduisez les messages visibles avec `useTranslate` ou votre bibliothèque i18n avant de les transmettre au provider.
