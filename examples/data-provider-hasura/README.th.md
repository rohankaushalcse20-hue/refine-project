# ตัวอย่าง Refine data provider สำหรับ Hasura

ตัวอย่างนี้แสดงการใช้ Hasura และ GraphQL กับ Refine ผ่าน `dataProvider` เพื่อให้หน้าจอ CRUD ใช้ query และ mutation จาก backend ได้โดยยังคงโครงสร้าง resource ของ Refine

## จุดสำคัญ

- เชื่อม Refine กับ Hasura GraphQL API
- ใช้ `dataProvider` เพื่อแปลง CRUD operation เป็น GraphQL request
- คงชื่อ query, mutation, resource และ package ตามต้นฉบับ
- เหมาะสำหรับทีมที่ใช้ GraphQL schema เป็นชั้นข้อมูลหลัก

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example data-provider-hasura
```

## เปิดบน CodeSandbox

[![Open data-provider-hasura example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-hasura?view=preview&theme=dark&codemirror=1)
