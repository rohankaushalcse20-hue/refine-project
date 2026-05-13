---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Çevirileri, aktif locale bilgisini ve dil değiştirmeyi Refine'a nasıl bağlayacağınızı öğrenin."
---

`i18nProvider`, Refine'ı seçtiğiniz internationalization library ile bağlar. Bu provider, Refine'a metin çevirme, aktif locale'i okuma ve dili değiştirme yolu sağlar.

## Provider sözleşmesi

Provider genellikle `translate`, `changeLocale` ve `getLocale` metotlarını sağlar. Implementasyon `i18next`, `react-intl`, kurum içi message formatı veya başka bir translation sistemi kullanabilir.

```tsx title=i18nProvider.ts
export const i18nProvider = {
  translate: (key, params, defaultMessage) => defaultMessage ?? key,
  changeLocale: (locale) => Promise.resolve(locale),
  getLocale: () => "tr",
};
```

## `useTranslate` kullanma

`useTranslate` hook'u provider'daki translation fonksiyonunu alır. Menü etiketleri, sayfa başlıkları, form mesajları, notifications ve kullanıcıya görünen diğer metinler için bu hook'u kullanın.

```tsx
const translate = useTranslate();

translate("posts.fields.title", "Title");
```

## Locale değiştirme

`changeLocale`, language switcher içinden çağrılabilir. Uygulama locale tabanlı route kullanıyorsa dil değiştirmenin navigasyonu router ile tutarlı tuttuğundan emin olun.

## API'ı stabil tutma

Translation key'leri stabil olmalı ve görüntülenen metne bağlı kalmamalıdır. Böylece component'leri, resources tanımlarını veya route yapılarını değiştirmeden çevirileri iyileştirebilirsiniz.
