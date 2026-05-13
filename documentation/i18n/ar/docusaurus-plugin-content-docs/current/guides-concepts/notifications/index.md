---
title: "الإشعارات | Refine v5"
display_title: "الإشعارات"
sidebar_label: "الإشعارات"
description: "اعرض رسائل النجاح والخطأ والتنبيه باستخدام notification provider في Refine."
---

الإشعارات مناسبة لتأكيد نجاح العملية أو شرح سبب الفشل. يستخدم Refine `notificationProvider` لعرض الرسائل من داخل الـ hooks والـ mutations والـ components.

## Notification provider

غالباً ما يوفّر هذا الـ provider دالة `open` لعرض الرسالة، ودالة `close` لإغلاقها عند الحاجة.

```tsx
const notificationProvider = {
  open: ({ type, message, description }) => {
    console.log(type, message, description);
  },
  close: (key) => {
    console.log("close", key);
  },
};
```

## تكاملات واجهات الاستخدام

إذا كنت تستخدم Ant Design أو Material UI أو Mantine أو Chakra UI، فيمكنك وصل نظام الإشعارات الخاص بهذه المكتبات مباشرةً إلى Refine.

## i18n

في التطبيقات المحلية ينبغي أن تتوافق رسائل النجاح والخطأ والتحذير مع لغة الواجهة، لذلك من المهم ترجمة عناوين الإشعارات ووصفها أيضاً.
