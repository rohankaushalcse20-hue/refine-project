# @refinedev/simple-rest

`@refinedev/simple-rest` ให้ data provider สำหรับ REST API แบบเรียบง่าย โดยแปลง operation ของ Refine เช่น `getList`, `getOne`, `create`, `update` และ `deleteOne` เป็น HTTP request ตาม convention ของ package

## Package นี้มีอะไร?

- Method พื้นฐานของ `dataProvider` สำหรับ REST resources
- รองรับ pagination, sorting และ filtering ที่ส่งมาจาก hooks ของ Refine
- จุดเริ่มต้นขนาดเล็กสำหรับ examples, prototypes และ API ที่มี endpoint คาดเดาได้

## ใช้เมื่อใด?

ใช้ provider นี้เมื่อ backend REST ของคุณตรงกับ contract แบบง่าย หรือเมื่อต้องการเริ่มแอป Refine อย่างรวดเร็วก่อนเขียน `dataProvider` เอง Method name, endpoint และ package name ไม่ควรถูกแปล
