---
id: otpLogin
title: "OtpLogin 示例 | Refine v5 最佳实践"
display_title: "OTP Login"
sidebar_label: "OTP Login"
description: "在 Refine v5 中安全实现 OtpLogin。学习面向真实 React 管理面板的 OAuth、JWT 最佳实践，并查看实用代码示例。"
example-tags: [auth-provider]
---

一次性密码（OTP）是一种具备两个基本特性的密码：它会很快过期，并且不能重复使用。OTP 通常是数字或字母数字字符串，并为单次登录流程生成。本示例展示如何在 Refine 中使用 OTP 输入逻辑。你可以通过 Refine [AuthProvider](/core/docs/authentication/auth-provider/) 使用一次性密码访问应用。

<CodeSandboxExample path="auth-otp" />
