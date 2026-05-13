---
title: "Authentication | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "เชื่อม Refine กับระบบเข้าสู่ระบบผ่าน authProvider."
---

Refine จัดการ authentication ผ่าน `authProvider` provider นี้อธิบายวิธี login, logout, ตรวจสอบ session, อ่าน identity ของผู้ใช้ และจัดการ error ด้านการยืนยันตัวตน

## Auth provider

`authProvider` มัก implement method เช่น `login`, `logout`, `check`, `getIdentity`, `onError` และ `forgotPassword` คุณสามารถเชื่อมกับ cookie session, JWT, OAuth, Auth0, Supabase Auth หรือระบบภายในได้

```tsx
const authProvider = {
  login: async ({ email, password }) => {
    // call your auth API
    return { success: true, redirectTo: "/" };
  },
  logout: async () => ({ success: true, redirectTo: "/login" }),
  check: async () => ({ authenticated: true }),
  getIdentity: async () => ({ id: 1, name: "Jane Doe" }),
  onError: async () => ({ error: null }),
};
```

## Protected routes

เมื่อใช้ router integration Refine สามารถพาผู้ใช้ที่ยังไม่ authenticated ไปหน้า login และส่งกลับมายัง route เดิมหลัง login สำเร็จ

## User identity

`getIdentity` ให้ข้อมูลสำหรับแสดงผล เช่น ชื่อ avatar หรือ email UI framework integrations สามารถใช้ข้อมูลนี้ใน layout, account menu หรือ audit trail

## Localization

ข้อความ error ตอน login, label ของ form และ status text ควรถูกแปลผ่าน `i18nProvider` หรือระบบ translation ของแอป ส่วนชื่อ method ใน `authProvider` ต้องคงเดิม
