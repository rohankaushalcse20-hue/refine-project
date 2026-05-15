# refine 的 React Hook Form 集成

`@refinedev/react-hook-form` 将 refine 的表单流程集成到 [React Hook Form](https://react-hook-form.com/)。它帮助创建新增和编辑页面，同时保留校验、状态以及对 data provider 的调用。

## 安装

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## 基本用法

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

## 文档

- 查看 refine 的 [`useForm` 文档](https://refine.dev/docs/packages/documentation/react-hook-form/useForm/)。
- 阅读 [refine 教程](https://refine.dev/docs/tutorial/introduction/index/)。
