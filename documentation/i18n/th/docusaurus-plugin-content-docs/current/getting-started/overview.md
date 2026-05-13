---
title: "Overview | Refine v5"
display_title: "ภาพรวม"
sidebar_label: "ภาพรวม"
description: "ทำความเข้าใจแนวคิดหลักของ Refine ก่อนเริ่มสร้างแอป React ที่เน้น CRUD."
displayed_sidebar: mainSidebar
slug: /getting-started/overview
---

**Refine** เป็น headless framework สำหรับสร้างแอป React ที่ทำงานกับข้อมูลจำนวนมากได้อย่างรวดเร็ว เหมาะกับ admin panel, internal tool, dashboard, พอร์ทัล B2B และ workflow แบบ CRUD ที่ต้องมีการอ่านข้อมูล form, table, routing, authentication และ authorization ในสถาปัตยกรรมเดียวกัน

Refine ให้คุณควบคุมชั้น UI ได้เอง คุณสามารถใช้ Ant Design, Material UI, Mantine, Chakra UI, Tailwind CSS, design system ของทีม หรือใช้เฉพาะส่วน headless ผ่าน `@refinedev/core`

## ทำไมต้อง Refine?

- **Headless core:** logic ด้านข้อมูล state และ navigation แยกจาก UI framework
- **สถาปัตยกรรม provider:** `dataProvider`, `authProvider`, `accessControlProvider`, `notificationProvider`, `i18nProvider` และ router provider ทำให้เปลี่ยน integration ได้เป็นส่วน ๆ
- **เพิ่มผลผลิตของ CRUD:** มีรูปแบบร่วมสำหรับ action เช่น `list`, `show`, `create`, `edit` และ `clone`
- **รองรับงานจริง:** รองรับ filtering, pagination, optimistic updates, realtime, audit logs และ multi-tenancy

## โครงสร้างพื้นฐาน

แอป Refine มักถูกออกแบบรอบ `resources` และ `providers` โดย `resources` อธิบาย entity ของโดเมน ส่วน `providers` เชื่อมแอปกับข้อมูล การยืนยันตัวตน notification และ routing

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        create: "/products/new",
        edit: "/products/:id/edit",
        show: "/products/:id",
      },
    ]}
  />
);
```

## ขั้นตอนถัดไป

หากต้องการสร้างโปรเจกต์ใหม่ ให้ไปที่ [Quickstart](/core/docs/getting-started/quickstart/) หากต้องการเข้าใจสถาปัตยกรรมให้ลึกขึ้น เริ่มจาก [General Concepts](/core/docs/guides-concepts/general-concepts/) และ [Data Fetching](/core/docs/guides-concepts/data-fetching/)
