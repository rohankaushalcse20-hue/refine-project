---
title: "النماذج | Refine v5"
display_title: "النماذج"
sidebar_label: "النماذج"
description: "ابنِ نماذج CRUD في Refine مع hooks وعمليات validation وواجهات UI مختلفة."
---

النماذج هي جوهر التفاعل في تطبيقات CRUD. يوفّر Refine hooks وcomponents تربط بين الحقول وعمليات mutations والـ data providers بطريقة منظّمة.

## الأساسيات

يمكنك العمل مع Ant Design أو Material UI أو Mantine أو Chakra UI أو React Hook Form. منطق Refine مستقل عن طبقة العرض، لذا يمكنك اختيار المكتبة الأنسب لتجربة المنتج.

## الإنشاء والتعديل

بمساعدة `useForm` و`useModalForm` و`useDrawerForm` و`useStepsForm` يمكنك تنظيم مسارات create وedit أو النماذج متعددة الخطوات.

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
});
```

## الحقول المرتبطة

تسهل `useSelect` جلب الخيارات من resource آخر، وهو ما يفيد عند التعامل مع العلاقات وfilters والبحث البعيد.

## التحقق من الصحة

من الأفضل الجمع بين validation المحلي ورسائل الأخطاء العائدة من الخادم. وفي التطبيقات متعددة اللغات، يجدر توحيد النصوص عبر i18n provider حتى تبقى الرسائل واضحة ومتسقة.
