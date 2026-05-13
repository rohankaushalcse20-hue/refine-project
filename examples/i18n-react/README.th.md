# ตัวอย่าง Refine i18n React

ตัวอย่างนี้แสดงวิธีเชื่อม Refine กับแอป React ที่รองรับหลายภาษา จุดสำคัญคือ `i18nProvider`, การเลือก locale และการรักษา translation keys ให้สอดคล้องกันในหน้าจอ CRUD

## จุดสำคัญ

- Integrate `i18nProvider` กับแอป React
- แสดงวิธีเปลี่ยน locale สำหรับ text ที่แสดง โดยไม่เปลี่ยน resource หรือ API name
- คง package name, path, command และ API ในรูปเดิม
- เหมาะเป็นจุดเริ่มต้นสำหรับ admin panel หลายภาษา

## รันตัวอย่าง

```sh
npm install
npm run dev
```

## ใช้เมื่อใด?

ใช้ตัวอย่างนี้เมื่อแอป Refine ของคุณต้องรองรับหลายภาษาใน React แต่ยังต้องการให้การตั้งค่า `resources`, providers และ CRUD flow คงที่
