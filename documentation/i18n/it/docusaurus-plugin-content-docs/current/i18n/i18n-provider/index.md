---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Gestisci traduzioni, cambio locale e UI multilingua nelle applicazioni Refine con i18n provider."
---

Refine astrae i testi dell'applicazione e il comportamento locale tramite `i18nProvider`. Questo provider collega la tua libreria di traduzione agli hooks e ai componenti UI di Refine con un contratto comune.

## Contratto di base

`i18nProvider` di solito espone `translate`, `changeLocale` e `getLocale`. Refine può usare questi metodi per menu, button, titoli pagina e componenti personalizzati.

```ts title=i18nProvider.ts
export const i18nProvider = {
  translate: (key, params) => i18n.t(key, params),
  changeLocale: (lang) => i18n.changeLanguage(lang),
  getLocale: () => i18n.language,
};
```

## Uso delle traduzioni

`useTranslate` viene usato per leggere chiavi di traduzione nell'applicazione. Questo hook offre un'API coerente lato Refine, indipendente dalla libreria i18n scelta.

## Cambio locale

Con `changeLocale` puoi cambiare la lingua scelta dall'utente. Questa scelta può essere supportata da URL, local storage, cookie o un altro metodo di persistenza preferito dall'applicazione.

## Testi delle resource

Etichette delle resource, testi delle action e titoli pagina personalizzati possono essere gestiti con chiavi i18n. In questo modo le schermate CRUD mantengono lo stesso modello resource nelle applicazioni multilingua.
