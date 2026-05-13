---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Verbind Refine met je vertaalbibliotheek via het i18nProvider-contract."
displayed_sidebar: mainSidebar
slug: /i18n/i18n-provider
---

De `i18nProvider` koppelt Refine aan de vertaaloplossing van je applicatie. Daarmee kunnen resources, knoppen, meldingen en custom UI dezelfde taalinstellingen gebruiken.

## Contract

Een `i18nProvider` bevat meestal `translate`, `changeLocale` en `getLocale`. Je kunt deze methoden verbinden met libraries zoals i18next, react-intl of een eigen vertaalservice.

```ts
export const i18nProvider = {
  translate: (key: string, params?: object) => i18n.t(key, params),
  changeLocale: (locale: string) => i18n.changeLanguage(locale),
  getLocale: () => i18n.language,
};
```

## Vertaalkeys

Gebruik stabiele keys voor resource labels, acties en meldingen. Vermijd het hardcoderen van displayteksten in componenten wanneer dezelfde tekst ook elders in de applicatie nodig is.

## Locale wisselen

Met `changeLocale` kun je een taalkeuze in de UI verbinden met de vertaalbibliotheek. Bewaar de keuze eventueel in local storage, cookies of gebruikersvoorkeuren.

## Samenwerking met Docusaurus

De documentatiesite gebruikt Docusaurus-lokalisatie. Applicaties die je met Refine bouwt, gebruiken hun eigen `i18nProvider`; beide patronen houden teksten gescheiden van code en route-structuur.
