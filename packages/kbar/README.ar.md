# تكامل kbar مع Refine

تضيف حزمة `@refinedev/kbar` لوحة أوامر مبنية على [kbar](https://github.com/timc1/kbar) إلى تطبيقات Refine. وهي مفيدة لتوفير تنقل سريع بين resources وactions والشاشات.

## التثبيت

```sh
npm install @refinedev/kbar
```

## الاستخدام الأساسي

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";

const App = () => (
  <RefineKbarProvider>
    <Refine>{/* ... */}</Refine>
    <RefineKbar />
  </RefineKbarProvider>
);
```

يحافظ التكامل على مزامنة actions الخاصة بـ Refine مع تجربة البحث والتنقل داخل لوحة الأوامر.

## التوثيق

راجع [مثال command palette في Refine](https://refine.dev/docs/examples/command-palette/) لخيارات الإعداد والاستخدام.
