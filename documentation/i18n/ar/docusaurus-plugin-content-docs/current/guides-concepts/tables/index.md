---
title: "الجداول والقوائم | Refine v5"
display_title: "الجداول"
sidebar_label: "الجداول"
description: "كيف تبني Tables وLists مع pagination وfiltering وsorting في Refine."
---

الجداول والقوائم تجعل بيانات الـ API أسهل في القراءة والتنفيذ. يوفّر Refine hooks تربط pagination وfilters وsorting بحالة التحميل ومصدر البيانات.

## عرض القوائم

`useTable` و`useList` هما أكثر نقاط البداية شيوعاً. يمكنك استخدامهما مع تكاملات UI الجاهزة أو مع components مخصّصة بالكامل.

```tsx
const table = useTable({
  resource: "products",
  pagination: { pageSize: 10 },
});
```

## الفرز والتصفية

يحوّل Refine الـ filters والـ sorters إلى معلمات يمكن للـ data provider إرسالها إلى الـ API، ما يقلل من الربط المباشر بين تفاصيل الواجهة وطريقة التخاطب مع الخادم.

## إجراءات CRUD

يمكنك دمج أزرار create وedit وshow وdelete داخل القوائم. هذه الإجراءات يمكن أن تحترم قرارات `accessControlProvider`، كما يمكن ترجمة labels الخاصة بها عبر i18n.

## تجربة الاستخدام

تعامل بوضوح مع loading state وempty state وerror state، وفكّر في pagination أو التحميل التدريجي عندما تصبح البيانات كبيرة.
