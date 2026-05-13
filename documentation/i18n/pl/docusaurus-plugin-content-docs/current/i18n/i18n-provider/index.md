---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Podłącz tłumaczenia i zmianę języka przez kontrakt i18nProvider."
slug: /i18n/i18n-provider
---

`i18nProvider` łączy Refine z biblioteką tłumaczeń używaną w aplikacji. Refine nie wymusza konkretnego rozwiązania, więc możesz użyć `react-i18next`, `next-intl`, `formatjs` albo własnego mechanizmu.

## Kontrakt

Provider zwykle udostępnia metody `translate`, `changeLocale` i `getLocale`. Dzięki nim komponenty Refine oraz kod aplikacji mogą pobierać teksty i zmieniać aktualny język w spójny sposób.

```tsx title=App.tsx
<Refine
  i18nProvider={{
    translate: (key, params) => i18n.t(key, params),
    changeLocale: (lang) => i18n.changeLanguage(lang),
    getLocale: () => i18n.language,
  }}
/>
```

## Klucze tłumaczeń

Warto używać stabilnych kluczy, na przykład `resources.products.fields.name`. Klucze są bezpieczniejsze niż tłumaczenie po tekście źródłowym, ponieważ można zmieniać treść UI bez naruszania kontraktu komponentów.

## Resources i akcje

Tłumaczenia resource mogą obejmować etykiety w menu, tytuły stron, nazwy pól i komunikaty akcji. Dzięki temu lista, formularz i powiadomienia korzystają z tego samego słownika domenowego.

## Zmiana locale

`changeLocale` powinno aktualizować bibliotekę i18n oraz, jeśli aplikacja tego wymaga, zapisywać wybór użytkownika w URL, cookie albo profilu. W aplikacjach Next.js i Remix wybór locale może też wpływać na routing.

## Praktyczna wskazówka

Oddziel tłumaczenia domenowe od tekstów technicznych. Nazwy API, importy, komendy i identyfikatory powinny pozostać bez zmian, a tłumaczone powinny być tylko teksty widoczne dla użytkownika.
