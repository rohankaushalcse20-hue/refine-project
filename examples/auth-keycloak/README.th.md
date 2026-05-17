# ตัวอย่าง Refine Keycloak authentication

ตัวอย่างนี้แสดงการใช้ Keycloak เป็น identity provider สำหรับแอป Refine โดยเน้นการเชื่อม token, session และการป้องกันหน้า resource ผ่าน `authProvider` โดยไม่เปลี่ยนโครงสร้าง CRUD ของแอป

## จุดสำคัญ

- ใช้ Keycloak สำหรับ login และ session management
- เชื่อมสถานะ authentication เข้ากับ Refine resource flow
- รักษาชื่อ package, endpoint และ API identifier ไว้ตามเดิม
- เหมาะสำหรับระบบภายในองค์กรที่ใช้ SSO หรือ realm ของ Keycloak

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## เปิดบน CodeSandbox

[![Open auth-keycloak example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
