---
title: "Notifications | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "ใช้ notificationProvider เพื่อแสดง feedback จาก mutation และ error ของแอป."
---

Refine ส่ง notification ผ่าน `notificationProvider` provider นี้เชื่อม mutation ที่สำเร็จ error warning หรือ message แบบกำหนดเองเข้ากับระบบ toast/snackbar ของแอป

## Notification provider

`notificationProvider` มักมี method `open` และ `close` UI integration สามารถ map ไปยัง Ant Design notification, Material UI snackbar, Mantine notifications หรือ library ภายในได้

```tsx
const notificationProvider = {
  open: ({ message, description, type }) => {
    // show notification
  },
  close: (key) => {
    // close notification
  },
};
```

## Mutation feedback

เมื่อ `create`, `update` หรือ `delete` สำเร็จ Refine สามารถแสดง notification ค่าเริ่มต้นได้ คุณยังปรับ message เป็นราย mutation หรือปิด notification ใน workflow ที่ต้องการความเงียบได้

## Error handling

Error จาก data provider หรือ auth provider สามารถแปลงเป็น notification ที่ผู้ใช้เข้าใจได้ เก็บรายละเอียดเชิงเทคนิคไว้ใน log และแสดง message ที่ชัดเจนใน UI

## แอปหลายภาษา

ในแอปที่มีหลาย locale text ของ notification ควรมาจาก `i18nProvider` หรือ translation system ของคุณเอง ส่วน CRUD action และ resource name ควรคงที่ใน code
