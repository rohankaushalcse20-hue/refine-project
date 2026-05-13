# ตัวอย่าง Refine i18n Next.js

ตัวอย่างนี้แสดงวิธีรวม Refine กับ routing และ localization ในแอป Next.js โดยเน้น `i18nProvider`, การเลือก locale และการรักษา translation keys ให้สอดคล้องกันระหว่าง pages และ resources

## จุดสำคัญ

- Integrate `i18nProvider` กับแอป Next.js
- แสดงให้เห็นว่า locale ส่งผลต่อ routing และ text ของ UI ได้อย่างไร
- คง package name, path, command และ API ในรูปเดิม
- เหมาะเป็นจุดเริ่มต้นสำหรับ admin app หลายภาษา

## รันตัวอย่าง

```sh
npm install
npm run dev
```

## ใช้เมื่อใด?

ใช้ตัวอย่างนี้เมื่อแอป Refine ทำงานบน Next.js และต้องเปลี่ยนภาษาโดยไม่ทำให้การตั้งค่า `resources`, providers และ CRUD pages เสียหาย
