# ตัวอย่าง Refine Kinde authentication

ตัวอย่างนี้แสดงการใช้ Kinde กับ Refine สำหรับ authentication ในแอป CRUD โดยให้ Kinde จัดการ identity และให้ Refine ใช้ `authProvider` เพื่อควบคุมสิทธิ์การเข้าถึงหน้าต่าง ๆ ของแอป

## จุดสำคัญ

- เชื่อม Kinde login กับ lifecycle ของ Refine
- รองรับการตรวจสถานะผู้ใช้และ redirect ตาม `authProvider`
- คงชื่อ command, import และ configuration key ตามต้นฉบับ
- เหมาะสำหรับ prototype หรือ internal tool ที่ต้องการ auth service สำเร็จรูป

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example auth-kinde
```

## เปิดบน CodeSandbox

[![Open auth-kinde example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
