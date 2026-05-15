# تكامل Airtable مع Refine

توفر حزمة `@refinedev/airtable` مزود بيانات لربط تطبيقات Refine بقواعد [Airtable](https://www.airtable.com/). وهي مناسبة لبناء لوحات داخلية وأدوات CRUD فوق بيانات موجودة مسبقاً في Airtable.

## التثبيت

```sh
npm install @refinedev/airtable
```

## الاستخدام الأساسي

```tsx
import dataProvider from "@refinedev/airtable";

const App = () => (
  <Refine dataProvider={dataProvider("API_KEY", "BASE_ID")}>
    {/* ... */}
  </Refine>
);
```

يحوّل الـ provider عمليات resources في Refine إلى استدعاءات ضد Airtable API من دون فرض مكتبة UI محددة.

## التوثيق

- راجع [توثيق data providers في Refine](https://refine.dev/docs/data/data-provider/).
- راجع [توثيق Refine الرئيسي](https://refine.dev/docs/) للأدلة والدروس.
