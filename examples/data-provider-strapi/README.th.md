# ตัวอย่าง Refine data provider สำหรับ Strapi

ตัวอย่างนี้แสดงการใช้ Strapi เป็น content backend ให้แอป Refine โดย `dataProvider` ช่วยให้ resource และ data hooks ทำงานกับ API ของ Strapi ได้โดยไม่ต้องกระจาย logic การเรียก API ไปทั่วแอป

## จุดสำคัญ

- ใช้ Strapi เป็นแหล่งข้อมูลสำหรับ CRUD screen
- แสดง pattern การเชื่อม `dataProvider` กับ backend ที่มี content type
- คงชื่อ endpoint, resource, command และ API identifier ตามเดิม
- เหมาะสำหรับ admin panel ที่จัดการ content จาก Strapi

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example data-provider-strapi
```

## เปิดบน CodeSandbox

[![Open data-provider-strapi example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-strapi?view=preview&theme=dark&codemirror=1)
