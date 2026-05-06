---
title: "I18n Provider | Refine v5"
display_title: "I18n Provider"
sidebar_label: "I18n Provider"
description: "अपनी पसंद की translation library को `i18nProvider` के माध्यम से Refine से जोड़ें।"
---

Refine किसी एक translation library को मजबूर नहीं करता। यह `i18nProvider` का उपयोग करता है, जो `react-i18next`, `next-i18next` या आपके internal solution को adapt कर सकता है।

## न्यूनतम interface

```tsx
const i18nProvider = {
  translate: (key, options, defaultMessage) => defaultMessage ?? key,
  changeLocale: (lang) => Promise.resolve(lang),
  getLocale: () => "hi",
};
```

Translations, menus, buttons और components को localized text देने के लिए provider को `<Refine />` में पास करें।

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

Translation lookups, language switching और current locale पढ़ने के लिए `useTranslate`, `useSetLocale` और `useGetLocale` का उपयोग करें।
