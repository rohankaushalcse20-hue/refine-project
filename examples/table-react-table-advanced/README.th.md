# ตัวอย่าง Refine advanced table กับ React Table

ตัวอย่างนี้แสดงการสร้าง table ที่ยืดหยุ่นด้วย React Table และ Refine สำหรับกรณีที่ต้องควบคุม column, filter, sorting และ pagination มากกว่าตารางสำเร็จรูปทั่วไป

## จุดสำคัญ

- ใช้ React Table ร่วมกับ data hooks ของ Refine
- แสดง pattern สำหรับ advanced filtering และ table state
- คงชื่อ hook, accessor, resource และ API identifier ตามต้นฉบับ
- เหมาะสำหรับหน้ารายการที่ต้องปรับแต่ง behavior ของตารางละเอียด

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example table-react-table-advanced
```

## เปิดบน CodeSandbox

[![Open table-react-table-advanced example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-react-table-advanced?view=preview&theme=dark&codemirror=1)
