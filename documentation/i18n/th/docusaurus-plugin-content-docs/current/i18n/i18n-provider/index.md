---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "เชื่อม Refine กับ library แปลภาษาที่คุณเลือกผ่าน i18nProvider."
---

`i18nProvider` เชื่อม Refine กับ library internationalization ที่คุณเลือก provider นี้บอก Refine ว่าจะแปล text อย่างไร อ่าน locale ปัจจุบันอย่างไร และเปลี่ยนภาษาอย่างไร

Refine ไม่บังคับ library ใด library หนึ่ง คุณสามารถใช้ `i18next`, `react-intl`, `next-intl`, message format ภายใน หรือระบบ translation ของทีม

```tsx title=i18nProvider.ts
export const i18nProvider = {
  translate: (key: string, options?: any, defaultMessage?: string) => {
    return defaultMessage ?? key;
  },
  changeLocale: (locale: string) => {
    return Promise.resolve();
  },
  getLocale: () => "th",
};
```

## ใช้กับ Refine

ส่ง provider เข้า `<Refine />` เพื่อให้ hooks และ UI integration ใช้แหล่ง translation เดียวกัน

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

## ควรแปลอะไร?

แปล label, notification, validation message, menu, title และ empty state อย่าแปล package name, import path, command, API identifier หรือ resource name ที่ backend ใช้

## เปลี่ยน locale

`changeLocale` ควรอัปเดต locale ใน library แปลภาษา และ sync กับ router หากแอปใช้ route ตาม locale ส่วน `getLocale` ช่วยให้ Refine รู้ locale ปัจจุบันเพื่อแสดง text ที่ถูกต้องใน UI
