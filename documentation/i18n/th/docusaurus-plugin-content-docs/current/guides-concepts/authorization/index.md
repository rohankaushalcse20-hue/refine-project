---
title: "Authorization | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "ใช้ accessControlProvider เพื่อควบคุมสิทธิ์ตาม resource และ action."
---

Authorization ใน Refine ทำผ่าน `accessControlProvider` provider นี้ตอบคำถามว่าผู้ใช้ปัจจุบันทำ action หนึ่งบน resource หรือ record ที่ระบุได้หรือไม่

## Access control provider

Method หลักคือ `can` ซึ่งรับ `resource`, `action`, `params` ที่เป็นตัวเลือก และส่งผลลัพธ์ว่าอนุญาตหรือปฏิเสธ

```tsx
const accessControlProvider = {
  can: async ({ resource, action, params }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Only admins can delete posts" };
    }

    return { can: true };
  },
};
```

## ซ่อนและบล็อก action

Refine ใช้ผล authorization เพื่อซ่อน button, บล็อก route หรือหยุด mutation ได้ วิธีนี้ช่วยให้ UI ไม่แสดง action ที่ผู้ใช้ไม่มีสิทธิ์ทำ

## สิทธิ์ระดับ record

ด้วย `params` คุณตรวจสอบสิทธิ์ตาม record ปัจจุบัน tenant, owner หรือสถานะทางธุรกิจได้ logic รายละเอียดยังคงอยู่ใน provider หรือ backend API

## หมายเหตุด้าน production

Authorization ฝั่ง UI ช่วยปรับประสบการณ์ผู้ใช้เท่านั้น Backend ยังต้องตรวจสิทธิ์ทุก request ข้อความปฏิเสธควรถูกแปลให้ผู้ใช้เข้าใจ แต่ key, action และ resource name ควรคงที่
