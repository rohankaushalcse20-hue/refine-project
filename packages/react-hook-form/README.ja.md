# React Hook Form integration for refine

`@refinedev/react-hook-form` は、React Hook Form を Refine の form workflow と連携するための package です。`useForm` から Refine の mutation、resource、redirect、保存状態を扱いながら、React Hook Form の柔軟なフォーム管理を利用できます。

## インストール

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## 基本的な使い方

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

## 使いどころ

複雑な validation、カスタム入力、既存の React Hook Form コンポーネントを使いながら、Refine の create/edit フローに接続したい場合に適しています。

## 詳細

- [refine React Hook Form documentation](https://refine.dev/docs/packages/documentation/react-hook-form/useForm/)
- [refine documentation](https://refine.dev/docs/)
- [refine tutorials](https://refine.dev/docs/tutorial/introduction/index/)
