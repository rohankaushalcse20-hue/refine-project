---
id: otpLogin
title: "ตัวอย่าง OtpLogin | แนวทางปฏิบัติที่ดีใน Refine v5"
display_title: "OTP Login"
sidebar_label: "OTP Login"
description: "รักษาความปลอดภัย OtpLogin ใน Refine v5 เรียนรู้แนวทางปฏิบัติที่ดีสำหรับ OAuth และ JWT ในแผงผู้ดูแลระบบ React ที่ใช้งานจริง"
example-tags: [auth-provider]
---

One-time password (OTP) คือรหัสผ่านที่มีคุณสมบัติหลักสองอย่าง: หมดอายุอย่างรวดเร็วและไม่สามารถใช้ซ้ำได้ โดยทั่วไป OTP เป็นสตริงตัวเลขหรือผสมตัวอักษรและตัวเลขที่สร้างขึ้นสำหรับขั้นตอนการเข้าสู่ระบบครั้งเดียว ตัวอย่างนี้แสดงวิธีใช้ตรรกะอินพุต OTP กับ Refine คุณสามารถใช้ one-time passwords เพื่อเข้าถึงแอปพลิเคชันด้วย Refine [AuthProvider](/core/docs/authentication/auth-provider/)

<CodeSandboxExample path="auth-otp" />
