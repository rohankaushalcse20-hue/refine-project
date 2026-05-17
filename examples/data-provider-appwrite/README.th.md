# ตัวอย่าง Refine data provider สำหรับ Appwrite

ตัวอย่างนี้แสดงการใช้ Appwrite เป็น backend สำหรับแอป Refine โดยใช้ `dataProvider` เพื่อจัดการ operation ของ resource และช่วยให้หน้าจอ CRUD ทำงานกับ collection ของ Appwrite ได้อย่างเป็นระบบ

## จุดสำคัญ

- ใช้ Appwrite กับ data hooks ของ Refine
- แสดงการจัดการ resource ผ่าน `dataProvider`
- รักษาชื่อ collection, package, command และ API name ตามตัวอย่างเดิม
- เหมาะสำหรับแอปที่ต้องใช้ backend service แบบครบชุด

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example data-provider-appwrite
```

## เปิดบน CodeSandbox

[![Open data-provider-appwrite example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-appwrite?view=preview&theme=dark&codemirror=1)
