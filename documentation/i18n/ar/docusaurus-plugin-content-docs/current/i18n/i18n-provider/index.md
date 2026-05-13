---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "اربط Refine بمكتبة الترجمة التي تختارها عبر i18nProvider."
---

# i18n Provider <GuideBadge id="guides-concepts/i18n" />

لا يفرض Refine مكتبة ترجمة محددة. يمكنك ربط `react-i18next` أو `next-i18next` أو أي حل مخصّص عبر `i18nProvider`.

## الواجهة الأساسية

```tsx
const i18nProvider = {
  translate: (key, options, defaultMessage) => defaultMessage ?? key,
  changeLocale: (lang) => Promise.resolve(lang),
  getLocale: () => "ar",
};
```

بعد تمرير هذا الـ provider إلى `<Refine />` ستتمكن الـ hooks والقوائم والأزرار والـ components من استخدام نفس آلية الترجمة.

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

## Hooks

استخدم `useTranslate` للحصول على دالة `translate`، و`useSetLocale` لتغيير اللغة، و`useGetLocale` لمعرفة اللغة النشطة حالياً.

## توصيات

حافظ على ثبات مفاتيح الترجمة، ولا تترجم المعرّفات التقنية، وجرّب النصوص الطويلة وصيغ الجمع والتواريخ والعملات ببيانات حقيقية داخل كل locale.
