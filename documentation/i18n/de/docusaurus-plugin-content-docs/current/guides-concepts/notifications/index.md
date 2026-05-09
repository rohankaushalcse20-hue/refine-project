---
title: "Benachrichtigungen | Refine v5"
display_title: "Benachrichtigungen"
sidebar_label: "Benachrichtigungen"
description: "Zeige ueber den Notification Provider von Refine Success- und Error-Meldungen an."
---

Benachrichtigungen helfen Nutzern dabei, Ergebnisse von Aktionen und auftretende Fehler sofort zu verstehen. Refine zeigt diese Meldungen ueber `notificationProvider` aus Hooks, Mutationen und Komponenten an.

## Notification Provider

Ein Provider stellt normalerweise `open` und haeufig auch `close` bereit.

```tsx
const notificationProvider = {
  open: ({ type, message, description }) => {
    console.log(type, message, description);
  },
  close: (key) => console.log("close", key),
};
```

Integrationen fuer Ant Design, Material UI, Mantine oder Chakra UI koennen ihre eigenen Notification-Systeme direkt mit Refine verbinden.

In einer lokalisierten Anwendung solltest du Titel und Beschreibungen uebersetzen, damit Feedback fuer die Zielgruppe klar lesbar bleibt.
