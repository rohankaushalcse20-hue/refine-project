# ตัวอย่าง Refine authentication กับ Material UI

ตัวอย่างนี้แสดงหน้า authentication สำหรับแอป Refine ที่ใช้ Material UI โดยรวม `authProvider` เข้ากับ layout และ component ของ Material UI เพื่อสร้างประสบการณ์ login ที่เข้ากับส่วนติดต่อผู้ใช้ของแอป

## จุดสำคัญ

- ใช้ Material UI สำหรับหน้า login และหน้าที่เกี่ยวข้องกับ auth
- แสดงการป้องกัน resource ด้วย `authProvider`
- คงชื่อ component, hook และ package ของ Refine และ Material UI ตามเดิม
- เหมาะสำหรับ dashboard ที่ต้องการ authentication พร้อม UI สำเร็จรูป

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example auth-material-ui
```

## เปิดบน CodeSandbox

[![Open auth-material-ui example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-material-ui?view=preview&theme=dark&codemirror=1)
