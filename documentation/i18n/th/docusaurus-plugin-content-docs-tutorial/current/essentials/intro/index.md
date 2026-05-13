---
title: "Intro | Refine Tutorial"
display_title: "บทนำ"
sidebar_label: "บทนำ"
description: "เตรียมตัวสำหรับ tutorial ของ Refine และทำความเข้าใจแอป CRUD ตัวอย่าง."
---

ใน tutorial นี้ คุณจะสร้างแอป Refine แบบลงมือทำจริง แต่ละขั้นเน้นส่วนเล็ก ๆ ของ CRUD workflow เพื่อให้เห็นว่า `resources`, providers, routing และ UI components ทำงานร่วมกันอย่างไร

## ก่อนเริ่ม

คุณควรคุ้นเคยกับ React, TypeScript เบื้องต้น และการรัน command ใน terminal คำสั่งอย่าง `npm create refine-app@latest`, `npm install` และ `npm run dev` จะคงรูปเดิมเพราะเป็น command ที่ต้องรันจริง

## แอปตัวอย่าง

แอปตัวอย่างใช้ resource เช่น `products` เพื่อสาธิต list, detail, create และ edit จากนั้นคุณสามารถใช้ pattern เดียวกันกับโดเมนจริง เช่น orders, customers หรือ tickets

## เป้าหมาย

หลังจบส่วน essentials คุณจะเข้าใจ:

- Refine แทน CRUD ด้วย `resources` อย่างไร
- `dataProvider` เชื่อม UI กับ backend อย่างไร
- วิธีเพิ่ม form และ table โดยไม่เขียน logic loading, mutation และ navigation ซ้ำ
- วิธีขยายแอปด้วย authentication, authorization และ i18n
