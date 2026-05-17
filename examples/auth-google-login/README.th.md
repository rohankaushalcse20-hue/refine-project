# ตัวอย่าง Refine Google login

ตัวอย่างนี้แสดงการเพิ่ม Google login ให้แอป Refine โดยใช้ authentication flow ที่คุ้นเคยสำหรับผู้ใช้และยังคงให้ Refine จัดการหน้า resource, redirect และสถานะการเข้าสู่ระบบผ่าน `authProvider`

## จุดสำคัญ

- เชื่อม Google login กับ flow ของ Refine
- คงชื่อ API, route และ provider configuration ตามตัวอย่างต้นฉบับ
- เหมาะสำหรับ dashboard ที่ต้องการ social login แบบรวดเร็ว
- ช่วยแยก logic ด้าน identity ออกจาก CRUD screen ของแอป

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example auth-google-login
```

## เปิดบน CodeSandbox

[![Open auth-google-login example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
