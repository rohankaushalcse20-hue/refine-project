# Refine Inferencer

تولّد حزمة `@refinedev/inferencer` واجهات CRUD من بنية بياناتك حتى تبدأ بسرعة ثم تعدّل الناتج يدوياً. وهي مفيدة خصوصاً عند استكشاف API أو بناء لوحة إدارة أولية.

## التثبيت

```sh
npm install @refinedev/inferencer
```

## الاستخدام الأساسي

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";

const App = () => {
  return (
    <Refine>
      <AntdInferencer action="list" resource="posts" />
    </Refine>
  );
};
```

## متى تستخدمها؟

استخدم Inferencer عندما تحتاج إلى prototyping سريع للشاشات أو فحص شكل API أو توليد نسخة أولى قابلة للتعديل من واجهات CRUD.

## المزيد

راجع توثيق Inferencer ودروس Refine لتكييف الواجهات المولدة مع مشروعك.
