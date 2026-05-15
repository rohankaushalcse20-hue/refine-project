# React Hook Form entegrasyonu

`@refinedev/react-hook-form`, Refine form workflow'larini [React Hook Form](https://react-hook-form.com/) ile birlestirir. `useForm`, `useModalForm` ve `useStepsForm` gibi yardimcilarla CRUD formlarini backend operasyonlarina baglamayi kolaylastirir.

## Kurulum

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## Temel kullanim

```tsx
import { useForm } from "@refinedev/react-hook-form";

const CreatePage = () => {
  const {
    refineCore: { onFinish },
    register,
    handleSubmit,
  } = useForm();

  return <form onSubmit={handleSubmit(onFinish)}>{/* ... */}</form>;
};
```

## Ne zaman kullanilmali?

React Hook Form'un validation, form state ve performans avantajlarini Refine'in resource ve mutation akislariyla birlikte kullanmak istediginizde bu package'i kullanin.

## Dokumantasyon

[Refine React Hook Form dokumantasyonu](https://refine.dev/docs/packages/react-hook-form/introduction/) kurulum, hook'lar ve ornek kullanimlari kapsar.
