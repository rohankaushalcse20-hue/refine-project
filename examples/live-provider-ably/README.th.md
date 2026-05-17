# ตัวอย่าง Refine live provider กับ Ably

ตัวอย่างนี้แสดงการเชื่อม Ably กับ Refine ผ่าน `liveProvider` เพื่อให้หน้าจอ resource ตอบสนองต่อ realtime event เช่นการสร้างหรือแก้ไขข้อมูลจากผู้ใช้อื่น

## จุดสำคัญ

- ใช้ Ably สำหรับ publish/subscribe event แบบ realtime
- เชื่อม event เข้ากับ `liveProvider` ของ Refine
- คงชื่อ `liveProvider`, `Ably` และ token placeholder ตามต้นฉบับ
- เหมาะสำหรับ dashboard ที่ต้องอัปเดตข้อมูลโดยไม่ต้อง refresh หน้า

## รันตัวอย่าง

```bash
npm create refine-app@latest -- --example live-provider-ably
```

## เปิดบน CodeSandbox

[![Open live-provider-ably example from refine](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/live-provider-ably?view=preview&theme=dark&codemirror=1)
