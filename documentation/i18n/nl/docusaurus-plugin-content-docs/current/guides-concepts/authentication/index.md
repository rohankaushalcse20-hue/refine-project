---
title: "Authentication | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "Beheer login, logout, sessiecontrole en gebruikersidentiteit met een authProvider."
displayed_sidebar: mainSidebar
slug: /guides-concepts/authentication
---

Authentication in Refine wordt afgehandeld via een `authProvider`. Deze provider centraliseert login, logout, sessiecontrole, foutafhandeling en het ophalen van gebruikersinformatie.

## Auth provider

Een `authProvider` kan methoden bevatten zoals `login`, `logout`, `check`, `getIdentity`, `onError`, `register`, `forgotPassword` en `updatePassword`. Je implementeert alleen wat je applicatie nodig heeft.

```ts
export const authProvider = {
  login: async ({ email, password }) => {
    // Authenticate against your API.
    return { success: true, redirectTo: "/" };
  },
  check: async () => {
    return { authenticated: true };
  },
  logout: async () => {
    return { success: true, redirectTo: "/login" };
  },
};
```

## Beschermde routes

Refine kan `check` gebruiken om te bepalen of een gebruiker toegang heeft tot een route. Routerintegraties gebruiken deze informatie om naar een loginpagina te redirecten of beschermde content weer te geven.

## Gebruikersidentiteit

Met `getIdentity` kun je profielinformatie tonen in layouts, headers of audit logs. Houd deze methode klein en voorspelbaar, bijvoorbeeld door alleen het id, de naam, het e-mailadres en de avatar terug te geven.

## Foutafhandeling

`onError` is nuttig wanneer API-verzoeken aangeven dat een sessie verlopen is. Je kunt dan tokens wissen, de gebruiker uitloggen of naar een loginroute sturen.
