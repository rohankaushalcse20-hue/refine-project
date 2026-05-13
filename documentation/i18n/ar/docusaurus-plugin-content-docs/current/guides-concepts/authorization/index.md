---
title: "التفويض | Refine v5"
display_title: "التفويض"
sidebar_label: "التفويض"
description: "تحكم في الوصول إلى actions وroutes وcomponents باستخدام access control provider."
---

التفويض يجيب عن سؤال: ماذا يستطيع المستخدم المصادق عليه أن يفعل؟ في Refine يتم ذلك عبر `accessControlProvider` الذي يقدّم قرارات الصلاحيات إلى الـ hooks والأزرار والقوائم والصفحات.

## Access control provider

الطريقة الأساسية هي `can`. تستقبل `resource` و`action` ومعلمات إضافية ثم تعيد ما إذا كان التنفيذ مسموحاً.

```tsx
const accessControlProvider = {
  can: async ({ resource, action }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Only admins can delete posts" };
    }

    return { can: true };
  },
};
```

## الاستخدام داخل الواجهة

يمكنك استخدام `useCan` لاتخاذ قرارات عرض ديناميكية بناءً على الصلاحيات.

```tsx
const { data } = useCan({ resource: "posts", action: "delete" });

return data?.can ? <DeleteButton /> : null;
```

## أفضل الممارسات

هذا الـ provider ممتاز لتحسين تجربة الواجهة ومنع إظهار الإجراءات غير المسموح بها، لكن التحقق النهائي من الصلاحيات يجب أن يبقى دائماً على مستوى الـ backend.
