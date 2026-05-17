# ตัวอย่าง Refine multipart upload กับ Material UI

ตัวอย่างนี้แสดงการอัปโหลดไฟล์แบบ multipart ในแอป Refine ที่ใช้ Material UI โดยเชื่อม form state, file input และ request payload เข้ากับ create หรือ edit flow ของ resource

## จุดสำคัญ

- แสดง pattern สำหรับ multipart file upload
- ใช้ Material UI สำหรับส่วนติดต่อผู้ใช้ของ form
- คงชื่อ field, endpoint, hook และ package ตามต้นฉบับ
- เหมาะสำหรับ resource ที่ต้องแนบรูปภาพ เอกสาร หรือไฟล์ประกอบ

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example upload-material-ui-multipart
```

## เปิดบน CodeSandbox

[![Open upload-material-ui-multipart example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/upload-material-ui-multipart?view=preview&theme=dark&codemirror=1)
