# ตัวอย่าง Refine `useTable` กับ Ant Design

ตัวอย่างนี้แสดงการใช้ `useTable` กับ Ant Design `Table` เพื่อสร้าง list page ที่รองรับ pagination, sorting และ filtering จาก data hooks ของ Refine

## จุดสำคัญ

- ใช้ `useTable` เพื่อจัดการข้อมูลสำหรับ Ant Design `Table`
- รองรับ pagination และ sorter ที่สอดคล้องกับ `dataProvider`
- คงชื่อ hook, component, resource และ API identifier ตามต้นฉบับ
- เหมาะสำหรับหน้ารายการข้อมูลใน admin panel ที่ใช้ Ant Design

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example table-antd-use-table
```

## เปิดบน CodeSandbox

[![Open table-antd-use-table example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-antd-use-table?view=preview&theme=dark&codemirror=1)
