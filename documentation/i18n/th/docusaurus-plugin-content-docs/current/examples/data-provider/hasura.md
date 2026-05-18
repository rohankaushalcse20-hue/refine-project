---
id: hasura
title: "ตัวอย่าง Hasura | การผสาน REST API ใน Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "ใช้งาน Hasura ใน Refine v5 เรียนรู้ขั้นตอนสำคัญและวิธีขยาย REST, GraphQL, API แบบกำหนดเอง และ data flow ที่ปรับขนาดได้"
example-tags: [data-provider, live-provider]
---

backend แบบ REST หรือ GraphQL ที่กำหนดเองสามารถผสานกับ Refine ได้ Refine มี [Hasura](https://hasura.io/) GraphQL Data Provider ให้พร้อมใช้งาน ด้วย Refine คุณสามารถเชื่อมต่อกับฐานข้อมูล Hasura สร้าง query เฉพาะ และใช้ข้อมูลได้อย่างสะดวก ตัวอย่างนี้แสดงรายละเอียดวิธีใช้ข้อมูลในฐานข้อมูล Hasura กับโปรเจกต์ Refine

## ชนิดข้อมูล ID

โดยค่าเริ่มต้น data provider จะถือว่าชนิด `ID` ของคุณคือ `uuid` คุณสามารถเปลี่ยนพฤติกรรมนี้ได้ด้วยตัวเลือก `idType` โดยส่ง `Int` หรือ `uuid` เป็นค่าของตัวเลือก `idType` หรือใช้ function เพื่อกำหนด `idType` ตามชื่อ resource

#### ส่งค่า 'Int' หรือ 'uuid' ให้ `idType`

วิธีนี้ช่วยให้กำหนด `idType` สำหรับทุก resource ได้

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### ส่ง function ให้ `idType`

วิธีนี้ช่วยให้กำหนด `idType` ตามชื่อ resource ได้

```tsx
const idTypeMap: Record<string, "Int" | "uuid"> = {
  users: "Int",
  posts: "uuid",
};

const myDataProvider = dataProvider(client, {
  idType: (resource) => idTypeMap[resource] ?? "uuid",
});
```

<CodeSandboxExample path="data-provider-hasura" />
