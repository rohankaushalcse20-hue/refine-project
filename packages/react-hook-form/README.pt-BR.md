# Integracao React Hook Form para refine

`@refinedev/react-hook-form` integra os fluxos de formulario do refine ao [React Hook Form](https://react-hook-form.com/). Ele ajuda a criar paginas de criacao e edicao preservando validacao, estado e chamadas ao data provider.

## Instalacao

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## Uso basico

```tsx
import { useForm } from "@refinedev/react-hook-form";

const EditPost = () => {
  const { register, handleSubmit, formState, refineCore } = useForm({
    refineCoreProps: {
      resource: "posts",
      id: "1",
    },
  });

  return; /* ... */
};
```

## Documentacao

- Consulte a [documentacao do useForm do refine](https://refine.dev/docs/packages/documentation/react-hook-form/useForm/).
- Veja os [tutoriais do refine](https://refine.dev/docs/tutorial/introduction/index/).
