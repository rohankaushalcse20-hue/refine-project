---
id: otpLogin
title: "Ví dụ OtpLogin | Thực hành tốt trong Refine v5"
display_title: "OTP Login"
sidebar_label: "OTP Login"
description: "Bảo vệ OtpLogin trong Refine v5. Tìm hiểu thực hành tốt cho OAuth, JWT trong bảng quản trị React thực tế qua các đoạn mã mẫu."
example-tags: [auth-provider]
---

Mật khẩu một lần (OTP) có hai đặc điểm cơ bản: hết hạn nhanh và không thể dùng lại. OTP thường là chuỗi số hoặc chữ-số, được tạo cho một quy trình đăng nhập duy nhất. Ví dụ này cho thấy cách dùng logic nhập OTP với Refine. Bạn có thể dùng mật khẩu một lần để truy cập ứng dụng thông qua [AuthProvider](/core/docs/authentication/auth-provider/) của Refine.

<CodeSandboxExample path="auth-otp" />
