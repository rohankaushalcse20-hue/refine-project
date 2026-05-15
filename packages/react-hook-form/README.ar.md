# تكامل React Hook Form مع Refine

تربط حزمة `@refinedev/react-hook-form` تدفقات النماذج في Refine مع [React Hook Form](https://react-hook-form.com/). تساعد على إنشاء resources وتعديلها والتحقق منها باستخدام hooks مألوفة من React Hook Form.

## التثبيت

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## الاستخدام الأساسي

```tsx
import { useForm } from "@refinedev/react-hook-form";

const ProductCreate = () => {
  const { register, handleSubmit, formState, refineCore } = useForm({
    refineCoreProps: {
      resource: "products",
      action: "create",
    },
  });

  return <form onSubmit={handleSubmit(refineCore.onFinish)}>{/* ... */}</form>;
};
```

## التوثيق

راجع [توثيق React Hook Form مع Refine](https://refine.dev/docs/packages/documentation/react-hook-form/useForm/) لخيارات validation والإرسال والمزامنة مع resources.
