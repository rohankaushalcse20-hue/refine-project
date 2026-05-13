---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Pelajari cara menghubungkan terjemahan, locale aktif, dan pergantian bahasa ke Refine."
---

`i18nProvider` menghubungkan Refine dengan library internationalization yang Anda pilih. Provider ini memberi Refine cara untuk menerjemahkan teks, membaca locale aktif, dan mengganti bahasa.

## Kontrak provider

Provider biasanya menyediakan `translate`, `changeLocale`, dan `getLocale`. Implementasinya dapat memakai `i18next`, `react-intl`, format message internal, atau sistem translation lain.

```tsx title=i18nProvider.ts
export const i18nProvider = {
  translate: (key, params, defaultMessage) => defaultMessage ?? key,
  changeLocale: (locale) => Promise.resolve(locale),
  getLocale: () => "id",
};
```

## Menggunakan `useTranslate`

Hook `useTranslate` mengambil fungsi translation dari provider. Gunakan hook ini untuk label menu, judul halaman, pesan form, notifikasi, dan teks lain yang terlihat pengguna.

```tsx
const translate = useTranslate();

translate("posts.fields.title", "Title");
```

## Pergantian locale

`changeLocale` dapat dipanggil dari language switcher. Jika aplikasi memakai route berbasis locale, pastikan pergantian bahasa juga menjaga navigasi tetap konsisten dengan router.

## Menjaga API tetap stabil

Kunci translation sebaiknya stabil dan tidak bergantung pada teks tampilan. Dengan begitu, Anda dapat memperbaiki terjemahan tanpa mengubah komponen, resources, atau route aplikasi.
