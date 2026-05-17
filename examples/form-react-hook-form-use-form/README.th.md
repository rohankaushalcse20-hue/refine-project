# ตัวอย่าง Refine `useForm` กับ React Hook Form

ตัวอย่างนี้แสดงการใช้ `useForm` จาก `@refinedev/react-hook-form` เพื่อเชื่อม form state, validation และ mutation ของ Refine เข้ากับ React Hook Form สำหรับหน้าสร้างหรือแก้ไข resource

## จุดสำคัญ

- ใช้ `useForm` ร่วมกับ React Hook Form
- เชื่อม submit flow เข้ากับ mutation ของ Refine
- คงชื่อ hook, package, field และ resource ตามต้นฉบับ
- เหมาะสำหรับ form ที่ต้องการควบคุม validation และ input registration เอง

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example form-react-hook-form-use-form
```

## เปิดบน CodeSandbox

[![Open form-react-hook-form-use-form example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-react-hook-form-use-form?view=preview&theme=dark&codemirror=1)
