# @refinedev/react-hook-form

`@refinedev/react-hook-form` เชื่อม Refine กับ React Hook Form เพื่อให้ form state, validation และ mutation ของ resource ทำงานร่วมกันได้ใน create, edit หรือ custom form page

## Package นี้มีอะไร?

- Hook เช่น `useForm`, `useModalForm` และ `useStepsForm`
- การเชื่อม `refineCoreProps` กับ mutation และ query ของ Refine
- รองรับการใช้ `register`, `handleSubmit` และ `formState` จาก React Hook Form
- เหมาะกับ form ที่ต้องควบคุม validation และ input behavior ละเอียด

## ติดตั้งและใช้งาน

```bash
npm install @refinedev/react-hook-form react-hook-form
```

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

## ใช้เมื่อใด?

ใช้ package นี้เมื่อคุณต้องการสร้าง form ของ Refine ด้วย React Hook Form โดยยังใช้ data hooks, mutation mode และ resource contract ของ Refine ตามเดิม
