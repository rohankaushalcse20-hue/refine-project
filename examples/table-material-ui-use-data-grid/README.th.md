# ตัวอย่าง Refine `useDataGrid` กับ Material UI

ตัวอย่างนี้แสดงการใช้ `useDataGrid` เพื่อเชื่อม Material UI Data Grid กับ resource ของ Refine โดยดูแล pagination, sorting และ filtering ผ่าน data provider เดียวกัน

## จุดสำคัญ

- ใช้ `useDataGrid` สำหรับ Material UI Data Grid
- เชื่อม server-side table state กับ hooks ของ Refine
- คงชื่อ hook, component, field และ resource ตามเดิม
- เหมาะสำหรับตารางข้อมูลที่ต้องรองรับ dataset ขนาดใหญ่

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example table-material-ui-use-data-grid
```

## เปิดบน CodeSandbox

[![Open table-material-ui-use-data-grid example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-material-ui-use-data-grid?view=preview&theme=dark&codemirror=1)
