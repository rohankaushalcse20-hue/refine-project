<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## مثال i18n مع React

يوضح هذا المثال كيف يمكن استخدام **Refine** داخل تطبيق React مع دعم internationalization. يتولى Refine منطق CRUD بينما تأتي النصوص المترجمة من `i18nProvider` المناسب.

## التشغيل محلياً

```bash
npm create refine-app@latest -- --example i18n-react
```

## ما الذي يستحق المراجعة؟

- إعداد `i18nProvider`
- تبديل اللغة من واجهة الاستخدام
- ترجمة القوائم والإجراءات والنصوص الظاهرة
- إبقاء `resources` و`routes` وواجهات الـ API كما هي

[افتح مثال i18n-react](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-react?view=preview&theme=dark&codemirror=1)
