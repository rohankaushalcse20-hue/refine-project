---
id: google-auth
title: "ตัวอย่าง Google Auth | Auth Provider ใน Refine v5"
display_title: "Google Auth"
sidebar_label: "Google Auth"
description: "สำรวจวิธีสร้างตัวอย่าง Google Auth ใน Refine v5 และวิธีใช้ provider สำหรับแผงผู้ดูแลระบบ React ที่ใช้งานจริง พร้อม snippet โค้ด"
example-tags: [auth-provider]
---

คุณสามารถใช้ Google Login เพื่อควบคุมการเข้าถึงและมอบ identity ให้แอปของคุณ ตัวอย่างนี้จะแนะนำวิธีเชื่อมต่อ Google Login เข้ากับโปรเจกต์โดยใช้ Refine

:::note

หากคุณกำลังพัฒนาแอป OAuth ของคุณเอง ควรเพิ่ม URL ของทั้งแอปที่ deploy แล้วและสภาพแวดล้อม local development ลงในรายการ allowed origins ของการตั้งค่า OAuth app หากไม่ทำเช่นนั้น แอปอาจทำงานล้มเหลว

สำหรับคำแนะนำแบบละเอียด คุณอาจดู [วิดีโอสอนนี้](https://www.youtube.com/watch?v=HtJKUQXmtok) เพิ่มเติมได้

:::

<CodeSandboxExample path="auth-google-login" />
