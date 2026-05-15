# Integracion de React Hook Form para Refine

`@refinedev/react-hook-form` conecta los flujos de formularios de Refine con [React Hook Form](https://react-hook-form.com/). Ayuda a crear, editar y validar recursos usando hooks conocidos de React Hook Form.

## Instalacion

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## Uso basico

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

## Documentacion

Consulta la [documentacion de React Hook Form para Refine](https://refine.dev/docs/packages/documentation/react-hook-form/useForm/) para opciones de validacion, envio y sincronizacion con recursos.
