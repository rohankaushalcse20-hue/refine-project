---
title: "General Concepts | Refine v5"
display_title: "แนวคิดทั่วไป"
sidebar_label: "แนวคิดทั่วไป"
description: "ทำความเข้าใจ resources, providers, hooks และ CRUD actions ใน Refine."
---

Refine จัดโครงสร้างแอปรอบแนวคิดหลักไม่กี่อย่าง เมื่อเข้าใจส่วนเหล่านี้ คุณจะเปลี่ยน UI framework, router หรือ backend ได้โดยไม่ต้องเขียน workflow CRUD ใหม่ทั้งหมด

## Resources

`resources` อธิบาย entity ทางธุรกิจ เช่น `products`, `orders` หรือ `users` แต่ละ resource สามารถประกาศ path สำหรับ action เช่น `list`, `create`, `edit`, `show` และ `clone`

```tsx
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
```

## Providers

Providers คือจุดเชื่อมต่อหลักของ Refine แอปจัดการ data, authentication, authorization, notifications, i18n, routing, realtime และ audit logs ผ่าน providers

ด้วยแนวทางนี้ หน้าจอ CRUD เดิมสามารถใช้ REST API วันนี้ เปลี่ยนเป็น GraphQL วันหน้า หรือเชื่อมกับ backend ภายในได้โดยยังคง API ฝั่ง UI ไว้

## Hooks และ components

Hooks เช่น `useList`, `useOne`, `useCreate`, `useUpdate` และ `useDelete` จัดการ state, cache, loading และ error ส่วน package UI อย่าง `@refinedev/mui` หรือ `@refinedev/antd` สร้าง component สำเร็จรูปบน hooks ชุดเดียวกัน

## CRUD actions

Refine ใช้ชุด action ที่สม่ำเสมอ ได้แก่ `list`, `show`, `create`, `edit`, `clone` และ `delete` action เหล่านี้ปรากฏใน routing, resource metadata, data provider และ UI component ทำให้แอปขยายจำนวน resource ได้ง่าย
