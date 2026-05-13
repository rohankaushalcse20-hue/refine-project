<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## مثال i18n مع Next.js

يعرض هذا المثال كيفية تشغيل **Refine** داخل مشروع Next.js مع طبقة ترجمة قابلة للتبديل. يفيد ذلك عندما تحتاج إلى صفحات CRUD مع routing وخيارات localization ضمن تطبيق SSR أو hybrid.

## التشغيل محلياً

```bash
npm create refine-app@latest -- --example i18n-nextjs
```

## ما الذي يوضحه المثال؟

- ربط Refine مع هيكل Next.js
- إعداد `i18nProvider` ضمن التطبيق
- إدارة اللغة النشطة والنصوص الظاهرة في الواجهة
- الحفاظ على commands وimports وأسماء الحزم كما هي

[افتح مثال i18n-nextjs](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-nextjs?view=preview&theme=dark&codemirror=1)
