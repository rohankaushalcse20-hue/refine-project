# أدوات Refine codemod

تحتوي حزمة `@refinedev/codemod` على transformations لتحديث مشاريع Refine بين الإصدارات وتطبيق تغييرات API الميكانيكية بعمل يدوي أقل.

## التثبيت والاستخدام

شغّل codemod من جذر مشروعك وراجع دائماً الـ diff الناتج قبل اعتماد التغييرات:

```sh
npx @refinedev/codemod
```

## متى تستخدمها؟

استخدم هذه الحزمة أثناء migrations أو التحديثات الكبيرة، خصوصاً عندما يغير إصدار من Refine imports أو أسماء الحزم أو الأنماط المتكررة في ملفات كثيرة.

## التوثيق

راجع [توثيق Refine الرئيسي](https://refine.dev/docs/) وملاحظات migration المناسبة قبل تشغيل transformations على فرع مشترك.
