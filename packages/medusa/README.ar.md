# تكامل Medusa Store

توفر حزمة `@refinedev/medusa` تكاملاً موجهاً للمتاجر ولوحات التشغيل المبنية على Medusa. تسمح بربط طبقة البيانات وتدفق authentication بإعداد أولي بسيط.

## التثبيت

```sh
npm install @refinedev/medusa
```

## الاستخدام الأساسي

```tsx
import dataProvider, { authProvider } from "@refinedev/medusa";

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider("API_URL")}
      authProvider={authProvider("API_URL")}
    >
      {/* ... */}
    </Refine>
  );
};
```

## متى تستخدمها؟

استخدمها عندما تحتاج إلى بناء أدوات داخلية أو dashboards أو لوحات إدارة لـ backend تجارة مبني على Medusa.

## المزيد

راجع توثيق Refine الرئيسي ومواد Medusa لتكييف authentication وresources وعمليات الكتالوج.
