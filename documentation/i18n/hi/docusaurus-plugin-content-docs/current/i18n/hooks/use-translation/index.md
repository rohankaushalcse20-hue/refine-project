---
title: "useTranslation Hook | Refine v5"
display_title: "useTranslation"
sidebar_label: "useTranslation"
description: "Refine v5 में useTranslation hook के जरिए translate, changeLocale और getLocale methods का Hindi परिचय।"
---

`useTranslation` hook आपको दिए गए [`i18nProvider`](/core/docs/i18n/i18n-provider/) से `translate`, `changeLocale` और `getLocale` methods तक पहुंच देता है। इसका उपयोग अपने components में text translate करने, locale बदलने और current locale प्राप्त करने के लिए किया जा सकता है।

## Usage

> यह hook तभी उपयोग किया जा सकता है जब [`i18nProvider`](/core/docs/i18n/i18n-provider/) configure किया गया हो।

```tsx
import { useTranslation } from "@refinedev/core";

export const MyComponent = () => {
  const { translate, getLocale, changeLocale } = useTranslation();
  const currentLocale = getLocale();

  return (
    <div>
      <h1>{translate("languages")}</h1>
      <button
        onClick={() => changeLocale("en")}
        disabled={currentLocale === "en"}
      >
        English
      </button>
      <button
        onClick={() => changeLocale("de")}
        disabled={currentLocale === "de"}
      >
        German
      </button>
    </div>
  );
};
```

## translate

यदि आपको अपने components में text translate करना है, तो `translate` method का उपयोग करें। यह अंदरूनी रूप से [`i18nProvider`](/core/docs/i18n/i18n-provider/) के `translate` method को call करता है।

```tsx
import { useTranslate } from "@refinedev/core";

export const MyComponent = () => {
  const translate = useTranslate();

  return <button>{translate("my.translate.text")}</button>;
};
```

## changeLocale

यदि runtime पर locale बदलना है, तो `changeLocale` method का उपयोग करें। यह अंदरूनी रूप से [`i18nProvider`](/core/docs/i18n/i18n-provider/) के `changeLocale` method को call करता है।

```tsx
import { useSetLocale } from "@refinedev/core";

export const LanguageSwicher = () => {
  const { changeLocale } = useTranslation();

  return (
    <div>
      <span>Languages</span>
      <button onClick={() => changeLanguage("en")}>English</button>
      <button onClick={() => changeLanguage("es")}>Spanish</button>
    </div>
  );
};
```

## getLocale

यदि current locale जानना है, तो `getLocale` method का उपयोग करें। यह अंदरूनी रूप से [`i18nProvider`](/core/docs/i18n/i18n-provider/) के `getLocale` method को call करता है।

```tsx
import { useSetLocale } from "@refinedev/core";

export const LanguageSwicher = () => {
  const { getLocale } = useTranslation();

  return <h1>Current Locale: {getLocale()}</h1>;
};
```
