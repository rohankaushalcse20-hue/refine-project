# Integrasi React Hook Form untuk Refine

Package `@refinedev/react-hook-form` menghubungkan workflow form Refine dengan [React Hook Form](https://react-hook-form.com/). Package ini membantu membuat, mengedit, dan memvalidasi resources menggunakan hooks yang familier dari React Hook Form.

## Instalasi

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## Penggunaan dasar

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

## Dokumentasi

Baca [dokumentasi React Hook Form dengan Refine](https://refine.dev/docs/packages/documentation/react-hook-form/useForm/) untuk opsi validation, submit, dan sinkronisasi dengan resources.
