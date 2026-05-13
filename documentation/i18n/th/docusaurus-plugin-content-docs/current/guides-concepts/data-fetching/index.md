---
title: "Data Fetching | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "เรียนรู้ data provider, data hooks และวิธีที่ Refine ทำให้การทำงานกับข้อมูลเป็นมาตรฐาน."
---

Data fetching ใน Refine ทำผ่าน `dataProvider` provider นี้แปลง action ของ Refine เป็น call ไปยัง REST, GraphQL, Supabase, Strapi หรือ backend ของคุณเอง

## Data provider

`dataProvider` มัก implement method เช่น `getList`, `getOne`, `create`, `update`, `deleteOne`, `getMany` และ `custom` Refine เรียก method เหล่านี้จาก hooks, UI component และ mutation flow

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/simple-rest";

export const App = () => (
  <Refine dataProvider={dataProvider("https://api.fake-rest.refine.dev")} />
);
```

## Data hooks

Hooks เช่น `useList`, `useOne`, `useMany`, `useCreate` และ `useUpdate` ให้ loading state, error state, cache และ mutation lifecycle ทำให้หน้าจอ CRUD ใช้ contract เดียวกันได้แม้ backend ต่างกัน

## Pagination, sorting และ filters

Refine ส่ง pagination, sorters และ filters ลงไปที่ `dataProvider` จากนั้น provider จะตัดสินใจว่าจะ map เป็น query string, request body หรือ GraphQL query อย่างไร

## ควรเขียน provider เองเมื่อใด?

เขียน `dataProvider` เองเมื่อ API ของคุณไม่ตรงกับ provider ที่มีอยู่ ต้องใช้ header พิเศษ หรือมีกฎ authorization ตาม tenant ให้รักษา method name และ shape ของข้อมูลตาม contract ของ Refine เพื่อให้ hooks และ components ทำงานต่อได้
