# React Hook Form integration for refine

`@refinedev/react-hook-form` Refine form workflows को React Hook Form के साथ जोड़ता है। इससे validation, field registration और submit handling React Hook Form से चलता है, जबकि resource mutation logic Refine core से जुड़ा रहता है।

## Installation

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## Basic usage

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

Complex forms में React Hook Form की ergonomics और Refine mutations दोनों चाहिए हों, तो यह package उपयोगी है।

अधिक जानकारी के लिए [React Hook Form package docs](https://refine.dev/docs/packages/documentation/react-hook-form/useForm/) देखें।
