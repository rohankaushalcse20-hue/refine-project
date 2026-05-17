# ตัวอย่าง Refine data provider สำหรับ Supabase

ตัวอย่างนี้แสดงการใช้ Supabase กับ Refine สำหรับ CRUD application โดย `dataProvider` เชื่อม data hooks ของ Refine เข้ากับตารางและ API ของ Supabase อย่างเป็นระบบ

## จุดสำคัญ

- ใช้ Supabase เป็น backend สำหรับ resource ของ Refine
- รองรับ list, create, edit และ show flow ผ่าน `dataProvider`
- รักษาชื่อ table, resource, package และ API name ตามต้นฉบับ
- เหมาะสำหรับแอปที่ต้องเริ่มจาก hosted Postgres และ API ของ Supabase

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example data-provider-supabase
```

## เปิดบน CodeSandbox

[![Open data-provider-supabase example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-supabase?view=preview&theme=dark&codemirror=1)
