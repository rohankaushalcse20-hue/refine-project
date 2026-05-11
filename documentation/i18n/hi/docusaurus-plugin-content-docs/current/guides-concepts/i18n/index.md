---
title: "I18n गाइड | Refine v5 में localization"
display_title: "Internationalization (i18n)"
sidebar_label: "Internationalization (i18n)"
description: "Refine v5 में i18n setup, translation files और locale switching को समझने के लिए Hindi guide."
---

import I18nHeadless from './i18n-headless.tsx';
import TranslationFileEN from '../../partials/\_partial-translation-file-en.md';
import TranslationFileDE from '../../partials/\_partial-translation-file-de.md';

Internationalization (i18n) वह प्रक्रिया है जिसके जरिए software applications को अलग-अलग भाषाओं और regions के लिए localize किया जाता है। Refine किसी भी i18n framework के साथ काम कर सकता है, लेकिन उसके लिए चुनी गई library के आधार पर एक [`i18nProvider`](/core/docs/i18n/i18n-provider/) देना जरूरी होता है।

## i18n Provider

[`i18nProvider`](/core/docs/i18n/i18n-provider/) Refine applications में localization process को centralize करता है। इसका interface flexible है, इसलिए आप `react-i18next`, `next-i18next` या किसी custom solution के साथ भी काम कर सकते हैं।

नीचे [react-i18next](https://react.i18next.com/) के साथ `i18nProvider` का मूल उदाहरण है:

<I18nHeadless />

## Example

:::simple Good to know

- इस example में UI library के रूप में [Ant Design](https://ant.design/) का उपयोग किया गया है, लेकिन आप कोई भी UI library चुन सकते हैं।
- हम `create refine-app` का उपयोग करने की सलाह देते हैं, क्योंकि CLI से project बनाते समय i18n support भी configure किया जा सकता है।
- अधिक जानकारी के लिए [react-i18next documentation&#8594](https://react.i18next.com/getting-started) देखें।
- यह example SPA React apps के लिए है; Next.js setup के लिए [i18n Next.js example&#8594][i18nnextjs] देखें।

:::

सबसे पहले Refine `i18nProvider` से यह shape अपेक्षित करता है:

```ts
import { I18nProvider } from "@refinedev/core";

const i18nProvider: I18nProvider = {
  translate: (key: string, options?: any, defaultMessage?: string) => string,
  changeLocale: (lang: string, options?: any) => Promise,
  getLocale: () => string,
};
```

इसके बाद `i18nProvider` को `<Refine />` component में pass किया जाता है:

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";

import i18nProvider from "./i18nProvider";

const App: React.FC = () => {
  return (
    <Refine
      // highlight-next-line
      i18nProvider={i18nProvider}
      /* ... */
    >
      {/* ... */}
    </Refine>
  );
};
```

यह setup होने के बाद [`useTranslation`][use-translation] hook translation features के लिए तैयार हो जाता है।

### Installation

`react-i18next` और `i18next` packages install करने के लिए यह command चलाएं:

<InstallPackagesCommand args="react-i18next i18next i18next-http-backend i18next-browser-languagedetector"/>

### Creating the i18n Instance

अब `react-i18next` के साथ i18n instance बनाएं:

```ts title="src/i18n.ts"
import i18n from "i18next";
import { initReactI18next } from "react-i18next";
import Backend from "i18next-http-backend";
import detector from "i18next-browser-languagedetector";

i18n
  .use(Backend)
  .use(detector)
  .use(initReactI18next)
  .init({
    supportedLngs: ["en", "de"],
    backend: {
      loadPath: "/locales/{{lng}}/{{ns}}.json",
    },
    ns: ["common"],
    defaultNS: "common",
    fallbackLng: ["en", "de"],
  });

export default i18n;
```

### Wrapping the app with React.Suspense

Translation bundles load होने तक fallback UI दिखाने के लिए application को `React.Suspense` से wrap किया जा सकता है:

```tsx title="src/index.tsx"
import React from "react";
import { createRoot } from "react-dom/client";
import App from "./App";

import "./i18n";

const container = document.getElementById("root");
const root = createRoot(container!);
root.render(
  <React.StrictMode>
    <React.Suspense fallback="loading">
      <App />
    </React.Suspense>
  </React.StrictMode>,
);
```

### Creating the i18n Provider

अब `useTranslation` hook से `t` और `i18n` लेकर Refine-compatible provider बनाएं:

```tsx title="src/App.tsx"
import type { I18nProvider } from "@refinedev/core";
import { Refine } from "@refinedev/core";
import { useTranslation } from "react-i18next";

const App: React.FC = () => {
  const { t, i18n } = useTranslation();

  const i18nProvider: I18nProvider = {
    translate: (key: string, options?: any) => t(key, options),
    changeLocale: (lang: string) => i18n.changeLanguage(lang),
    getLocale: () => i18n.language,
  };

  return (
    <Refine
      i18nProvider={i18nProvider}
      /* ... */
    >
      {/* ... */}
    </Refine>
  );
};
```

इसके बाद [`useTranslation`][use-translation] hook और Refine components दोनों एक ही translation source साझा करते हैं।

### Adding the Translation Files

Translation files आम तौर पर `public/locales/<locale>/common.json` structure में रखे जाते हैं:

```text
|-- public
|   |-- locales
|       |-- en
|       |   |-- common.json
|       |-- de
|           |-- common.json
```

Refine के default UI texts को override करने के लिए आप नीचे दिए गए translation keys का उपयोग कर सकते हैं:

<details>
<summary>English translation file</summary>

<TranslationFileEN />

</details>

<details>
<summary>German translation file</summary>

<TranslationFileDE />

</details>

### Locale switching

Active language बदलने के लिए `changeLocale` method या `useTranslation` hook का उपयोग किया जा सकता है। इससे menus, buttons, table labels और page titles जैसे texts runtime पर update हो सकते हैं।

### कब उपयोगी है

- multi-language admin panels
- region-specific internal tools
- apps जहां user-facing labels को translate करना जरूरी हो
- projects जिनमें business logic same रहे लेकिन UI language बदलती रहे

## Example

<CodeSandboxExample path="i18n-react" />

[i18nnextjs]: /core/docs/examples/i18n/i18n-nextjs
[use-translation]: /core/docs/i18n/hooks/use-translation
[create-refine-app]: /core/docs/getting-started/quickstart
