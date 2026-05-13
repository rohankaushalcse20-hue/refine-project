---
title: "Notifications | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "Toon consistente success-, error- en undo-meldingen via notificationProvider."
displayed_sidebar: mainSidebar
slug: /guides-concepts/notifications
---

Notificaties geven gebruikers feedback na mutaties, fouten en achtergrondacties. Refine gebruikt een `notificationProvider` zodat deze feedback consistent blijft, ongeacht de UI-bibliotheek.

## Notification provider

Een provider implementeert meestal `open` en `close`. Refine en je eigen code kunnen daarmee success-, error- en progress-meldingen tonen.

```ts
export const notificationProvider = {
  open: ({ message, description, type }) => {
    // Show a notification with your UI library.
  },
  close: (key) => {
    // Close the notification with this key.
  },
};
```

## Mutaties

Create-, update- en delete-acties kunnen automatisch notificaties tonen. Je kunt teksten per hook of per actie aanpassen wanneer de standaardmelding niet genoeg context geeft.

## Undoable acties

Bij `undoable` mutation mode is de notificatie ook een interactiepunt. De gebruiker krijgt tijd om de actie terug te draaien voordat de provider de mutatie definitief maakt.

## Richtlijn

Houd meldingen kort, concreet en actiegericht. Technische foutdetails horen meestal in logs; gebruikers hebben vooral nodig wat er is gebeurd en wat ze daarna kunnen doen.
