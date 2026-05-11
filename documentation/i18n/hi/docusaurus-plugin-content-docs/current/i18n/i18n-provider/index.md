---
title: "i18n Provider गाइड | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Refine में i18nProvider, translate, changeLocale और getLocale methods का Hindi परिचय।"
---

# i18n Provider <GuideBadge id="guides-concepts/i18n" />

Internationalization (i18n) applications को अलग-अलग भाषाओं और regions के लिए localize करने की प्रक्रिया है। Refine किसी भी i18n library के साथ काम कर सकता है, बशर्ते आप एक `i18nProvider` दें।

## Provider shape

```ts
import { I18nProvider } from "@refinedev/core";

const i18nProvider: I18nProvider = {
  translate: (key: string, options?: any, defaultMessage?: string) => string,
  changeLocale: (lang: string, options?: any) => Promise,
  getLocale: () => string,
};
```

`i18nProvider` को `<Refine />` में pass करने के बाद `useTranslation` जैसे hooks translation features का उपयोग कर सकते हैं।

## मुख्य methods

### translate

`translate` translation key लेकर localized string लौटाता है। जरूरत पड़ने पर इसमें `options` और `defaultMessage` भी दिया जा सकता है।

### changeLocale

`changeLocale` active language बदलने के लिए उपयोग होता है। यह अक्सर async होता है क्योंकि translation bundles lazy-load या persist किए जा सकते हैं।

### getLocale

`getLocale` वर्तमान locale लौटाता है, ताकि app language state को consistently पढ़ सके।

## Translation files

Refine components translation keys को override कर सकते हैं। इसलिए आप theme texts, menu labels, buttons, titles और table strings के लिए अपनी locale files बनाए रख सकते हैं।
