# @refinedev/ably

`@refinedev/ably` คือ live provider สำหรับเชื่อม Refine กับ Ably เพื่อรับ realtime event ในแอป CRUD package นี้ช่วยให้ resource สามารถตอบสนองต่อการเปลี่ยนแปลงข้อมูลจากผู้ใช้อื่นได้ผ่าน publish/subscribe flow

## Package นี้มีอะไร?

- `liveProvider` สำหรับส่ง event จาก Ably เข้าสู่ Refine
- การใช้งานร่วมกับ `Ably.Realtime`
- จุดเริ่มต้นสำหรับ dashboard ที่ต้องการ realtime updates
- ใช้ร่วมกับ provider อื่นของ Refine ได้โดยไม่ผูกกับ UI library

## ติดตั้งและใช้งาน

```bash
npm install @refinedev/ably
```

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");
```

## ใช้เมื่อใด?

ใช้ package นี้เมื่อแอป Refine ต้องรับ event แบบ realtime เช่น record ถูกสร้าง แก้ไข หรือลบจาก session อื่น ชื่อ package, import และ token placeholder ไม่ควรถูกแปล
