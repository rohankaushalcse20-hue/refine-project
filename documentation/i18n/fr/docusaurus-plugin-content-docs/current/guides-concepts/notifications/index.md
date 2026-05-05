---
title: "Notifications | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "Affichez les messages de succès et d'erreur avec le notification provider de Refine."
---

Les notifications confirment les actions et expliquent les erreurs. Refine utilise un `notificationProvider` pour afficher ces messages depuis hooks, mutations et composants.

## Notification provider

Un provider expose généralement `open` et parfois `close`.

```tsx
const notificationProvider = {
  open: ({ type, message, description }) => {
    console.log(type, message, description);
  },
  close: (key) => console.log("close", key),
};
```

Les intégrations Ant Design, Material UI, Mantine et Chakra UI peuvent connecter leur système de notifications à Refine.

Dans une application localisée, traduisez les titres et descriptions pour que les messages soient clairs dans la langue de l'utilisateur.
