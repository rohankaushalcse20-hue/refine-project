# ตัวอย่าง Refine Auth0 authentication

ตัวอย่างนี้แสดงการเชื่อม `authProvider` ของ Refine กับ Auth0 สำหรับแอป React ที่ต้องมี login, logout และการป้องกันหน้า resource จุดสำคัญคือการปล่อยให้ Auth0 ดูแล identity ขณะที่ Refine ใช้ผลลัพธ์นั้นกับ flow ของ CRUD

## จุดสำคัญ

- ตั้งค่า authentication ด้วย Auth0 โดยคงชื่อ provider และ API เดิม
- ใช้ `authProvider` เพื่อจัดการ session และ redirect หลัง login
- แสดงรูปแบบที่ต่อยอดไปใช้กับ resource ที่ต้องตรวจสิทธิ์ได้
- เหมาะสำหรับ admin panel ที่ต้องใช้ identity provider ภายนอก

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example auth-auth0
```

## เปิดบน CodeSandbox

[![Open auth-auth0 example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
