---
title: "Notifications | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "Configura notifiche di successo, errore e mutation annullabili in Refine con notification provider."
---

Notifications rendono visibili all'utente operazioni riuscite, errori e stati di mutation annullabili. Refine astrae questo comportamento con `notificationProvider`.

## Notification provider

`notificationProvider` fornisce i metodi necessari per aprire e chiudere notifiche. Ant Design, Material UI, Mantine, Chakra UI o un sistema toast personalizzato possono essere collegati tramite questo provider.

```ts title=notificationProvider.ts
export const notificationProvider = {
  open: ({ message, description, type }) => {
    // Mostra la notifica.
  },
  close: (key) => {
    // Chiudi la notifica.
  },
};
```

## Notifiche automatiche

Refine può attivare automaticamente notifiche di successo ed errore nelle mutation. I messaggi possono essere personalizzati tramite opzioni degli hooks o comportamento del provider.

## Operazioni undoable

Quando usi `undoable` mutation mode, le notifiche offrono all'utente la possibilità di annullare l'operazione. Questo pattern è utile soprattutto per eliminazioni o aggiornamenti critici.

## Messaggi di errore

Quando gli errori API vengono normalizzati dal data provider, il livello notification può mostrare messaggi più comprensibili. La traduzione dei dettagli tecnici in spiegazioni user-friendly avviene spesso a livello provider.
