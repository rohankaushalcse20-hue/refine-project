---
title: "Tables | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "สร้างรายการข้อมูลพร้อม pagination, sorting, filtering และ CRUD actions."
---

Table เป็นจุดเริ่มต้นที่พบบ่อยของแอป CRUD Refine มี hooks สำหรับ sync table กับ `dataProvider`, URL state และ resource metadata

## List hooks

ขึ้นอยู่กับ UI framework คุณอาจใช้ `useTable`, `useDataGrid` หรือ hook ที่เทียบเท่า hooks เหล่านี้เรียก `getList` และจัดการ pagination, sorters, filters และ loading state

```tsx
const { tableProps } = useTable({
  resource: "products",
});
```

## Row actions

ปุ่ม `ShowButton`, `EditButton`, `DeleteButton` หรือ custom action ใช้ resource route เพื่อนำทางไปยัง record ที่ถูกต้อง Authorization สามารถซ่อนหรือ disable action ได้เมื่อผู้ใช้ไม่มีสิทธิ์

## Filtering และ sorting

Filter และ sorter ควรถูกเก็บใน state ที่แชร์ผ่าน URL ได้เมื่อจำเป็น วิธีนี้ช่วยให้ผู้ใช้ refresh, แชร์ link หรือกลับมาที่ list โดยไม่เสีย context

## Localization

หัวคอลัมน์ empty state filter text และข้อความยืนยันการลบควรผ่าน translation system ส่วน field name, accessor และ API parameter ต้องคงเดิมเพื่อให้ data provider ทำงานได้ถูกต้อง
