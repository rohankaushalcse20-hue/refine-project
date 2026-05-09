---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Verbinde deine bevorzugte Uebersetzungsbibliothek ueber `i18nProvider` mit Refine."
---

Refine schreibt dir keine bestimmte Uebersetzungsbibliothek vor. Stattdessen arbeitet es mit einem `i18nProvider`, der `react-i18next`, `next-i18next` oder eine interne Loesung adaptieren kann.

## Minimale Schnittstelle

```tsx
const i18nProvider = {
  translate: (key, options, defaultMessage) => defaultMessage ?? key,
  changeLocale: (lang) => Promise.resolve(lang),
  getLocale: () => "de",
};
```

Uebergib den Provider an `<Refine />`, um Menues, Buttons und Komponenten mit lokalisiertem Text zu versorgen.

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

Fuer Uebersetzungen, Sprachwechsel und das Auslesen des aktuellen Locales nutzt du `useTranslate`, `useSetLocale` und `useGetLocale`.
