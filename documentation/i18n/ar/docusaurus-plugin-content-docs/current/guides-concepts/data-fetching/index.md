---
title: "جلب البيانات | Refine v5"
display_title: "جلب البيانات"
sidebar_label: "جلب البيانات"
description: "كيف يربط Refine الواجهة البرمجية عبر data providers وhooks موحّدة."
---

في التطبيقات الإدارية، تبقى البيانات هي المحور الأساسي. يربط Refine الواجهة بأي مصدر بيانات من خلال `dataProvider` يطبّق واجهة [`DataProvider`](/core/docs/core/interface-references#dataprovider).

يتلقى الـ data provider معلومات مثل `resource` و`id` و`meta` ثم يوجّه الطلب إلى endpoint المناسب.

## Hooks البيانات

بعد إعداد `dataProvider` يمكنك استخدام `useList` و`useOne` و`useCreate` و`useUpdate` و`useDelete` للتعامل مع عمليات CRUD.

```tsx
import { useOne } from "@refinedev/core";

const Product = () => {
  const { data, isLoading } = useOne({
    resource: "products",
    id: 1,
  });

  if (isLoading) return <span>Loading...</span>;
  return <pre>{JSON.stringify(data, null, 2)}</pre>;
};
```

## الحالة والتخزين المؤقت

تعتمد هذه الـ hooks داخلياً على TanStack Query، ما يمنحك حالات loading وerror وsuccess إلى جانب cache وrequest deduplication وautomatic invalidation.

## أكثر من provider

يمكنك أيضاً استخدام أكثر من provider داخل المشروع نفسه. على سبيل المثال قد يقرأ `posts` من REST بينما يستخدم `users` مزود GraphQL مع الحفاظ على نفس نمط الاستدعاء داخل التطبيق.
