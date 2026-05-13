---
title: "Authorization | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "Gebruik access control om resource-acties en UI-elementen per gebruiker te bewaken."
displayed_sidebar: mainSidebar
slug: /guides-concepts/authorization
---

Authorization bepaalt wat een ingelogde gebruiker mag doen. Refine gebruikt hiervoor een `accessControlProvider`, zodat rechten niet verspreid raken over losse componenten.

## Access control provider

De kernmethode is `can`. Deze krijgt een `resource`, een `action` en optioneel `params` mee. De methode retourneert of de actie is toegestaan en kan ook een reden teruggeven.

```ts
export const accessControlProvider = {
  can: async ({ resource, action, params }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Alleen beheerders mogen posts verwijderen." };
    }

    return { can: true };
  },
};
```

## UI en navigatie

Componenten en hooks kunnen dezelfde permissiecontrole gebruiken. Daarmee kun je knoppen verbergen, menu-items filteren of een fallback tonen zonder de autorisatielogica te kopiëren.

## Resource-acties

Gebruik consistente actienamen zoals `list`, `show`, `create`, `edit` en `delete`. Voor domeinspecifieke acties kun je eigen namen gebruiken, zolang je provider en UI dezelfde taal spreken.

## Praktische richtlijn

Laat de backend altijd de definitieve beveiliging afdwingen. De `accessControlProvider` maakt de frontend begrijpelijker en gebruiksvriendelijker, maar vervangt geen server-side authorization.
