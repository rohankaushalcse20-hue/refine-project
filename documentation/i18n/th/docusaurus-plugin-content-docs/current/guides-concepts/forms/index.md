---
title: "Forms | Refine v5"
display_title: "Forms"
sidebar_label: "Forms"
description: "สร้าง form สำหรับ create และ edit ด้วย hooks ของ Refine และ UI library ที่คุณเลือก."
---

Form ใน Refine เชื่อม mutation, validation, loading state และ navigation หลังบันทึก คุณสามารถใช้ UI integration ที่มีอยู่ หรือใช้ `@refinedev/core` ร่วมกับ form library ของคุณเอง

## Form hooks

Package UI มี hooks เช่น `useForm`, `useModalForm`, `useDrawerForm` และ `useStepsForm` hooks เหล่านี้ครอบ logic สำหรับโหลด record, submit mutation และจัดการ redirect

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
  id: 1,
});
```

## Create และ edit

ในหน้า `create` form ส่งข้อมูลผ่าน `dataProvider.create` ส่วนหน้า `edit` มักโหลด record ปัจจุบันก่อน แล้วส่งการเปลี่ยนแปลงผ่าน `dataProvider.update`

## Validation และ error

คุณใช้ validation ของ UI framework, schema validator หรือ error จาก backend ได้ Refine เก็บ mutation state เพื่อแสดง loading, disable ปุ่ม save และตอบสนอง error อย่างสม่ำเสมอ

## Select และข้อมูลสัมพันธ์

`useSelect` โหลด option จาก resource อื่น ให้รวม validation ฝั่ง client กับ error จาก server แล้วแปลข้อความผ่าน `i18nProvider` ในแอปหลายภาษา
