# ตัวอย่าง Refine `useForm` กับ Material UI

ตัวอย่างนี้แสดงการสร้าง form สำหรับแอป Refine ด้วย Material UI โดยใช้ `useForm` เพื่อเชื่อมข้อมูล resource, validation state และการ submit เข้ากับ component form ของ Material UI

## จุดสำคัญ

- ใช้ `useForm` สำหรับ create หรือ edit page
- แสดงการผูก Material UI input กับ state ของ Refine
- คงชื่อ component, hook, resource และ package ตามต้นฉบับ
- เหมาะสำหรับ dashboard ที่ใช้ Material UI เป็น UI layer หลัก

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example form-material-ui-use-form
```

## เปิดบน CodeSandbox

[![Open form-material-ui-use-form example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-material-ui-use-form?view=preview&theme=dark&codemirror=1)
