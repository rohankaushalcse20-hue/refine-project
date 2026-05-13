---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "เข้าใจวิธีเชื่อม resources ของ Refine กับ router provider และ path ของแอป."
---

Refine ไม่บังคับให้ใช้ router ตัวใดตัวหนึ่ง แอปสามารถใช้ React Router, Next.js, Remix หรือ integration ของคุณเองได้ ตราบใดที่ router provider ส่ง primitive ที่ Refine ต้องการ

## Resource routes

แต่ละ `resource` สามารถประกาศ route สำหรับ CRUD actions ได้ path เหล่านี้ถูกใช้โดย navigation, breadcrumbs, redirect หลัง mutation และ helper สำหรับสร้าง URL

```tsx
<Refine
  resources={[
    {
      name: "posts",
      list: "/posts",
      create: "/posts/create",
      edit: "/posts/edit/:id",
      show: "/posts/show/:id",
    },
  ]}
/>
```

## Router provider

`routerProvider` แปลงพฤติกรรม navigation ของ Refine ไปยัง router ที่คุณเลือก โดยทั่วไป provider จะอ่าน location ปัจจุบัน push route ใหม่ สร้าง link และ parse params

เมื่อเปลี่ยนจาก React Router ไป Next.js หรือ Remix คุณมักเก็บ resource metadata เดิมไว้ แล้วเปลี่ยนเฉพาะส่วน router integration

## Navigation ที่ควบคุมได้

Hooks และ components เช่น `useNavigation`, `CreateButton`, `EditButton` หรือ `ShowButton` ใช้ข้อมูล route จาก resource จึงทำให้ link ใน UI ตรงกับ route จริงของแอป

## หมายเหตุด้าน localization

หากแอปรองรับหลาย locale ให้คง API name, resource name และ route pattern ไว้เหมือนเดิม ส่วน text ที่แสดงต่อผู้ใช้ควรผ่าน `i18nProvider` หรือระบบ translation ของแอป
