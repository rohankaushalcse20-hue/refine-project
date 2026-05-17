# ตัวอย่าง Refine data provider สำหรับ Airtable

ตัวอย่างนี้แสดงการใช้ Airtable เป็น backend ให้แอป Refine ผ่าน `dataProvider` โดย map operation ของ CRUD ไปยังข้อมูลใน Airtable และยังคง resource configuration ของ Refine ให้อ่านง่าย

## จุดสำคัญ

- เชื่อม Refine กับ Airtable สำหรับ list, create, edit และ show flow
- แสดง pattern การตั้งค่า `dataProvider` สำหรับบริการภายนอก
- คงชื่อ field, resource, package และ API identifier ตามต้นฉบับ
- เหมาะสำหรับ dashboard ที่เริ่มจากฐานข้อมูล Airtable

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example data-provider-airtable
```

## เปิดบน CodeSandbox

[![Open data-provider-airtable example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-airtable?view=preview&theme=dark&codemirror=1)
