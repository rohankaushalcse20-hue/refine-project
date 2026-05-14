# React Hook Form integration for refine

`@refinedev/react-hook-form`은 React Hook Form을 Refine forms와 연결하는 helper hooks를 제공합니다. complex forms를 관리하면서 Refine의 resource, mutation, validation 흐름과 함께 사용할 수 있습니다.

## 설치

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## 기본 사용법

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

React Hook Form의 form state와 Refine의 CRUD mutations를 함께 쓰고 싶을 때 이 package를 선택하세요.

자세한 내용은 [refine React Hook Form documentation](https://refine.dev/docs/packages/documentation/react-hook-form/useForm/)을 참고하세요.
