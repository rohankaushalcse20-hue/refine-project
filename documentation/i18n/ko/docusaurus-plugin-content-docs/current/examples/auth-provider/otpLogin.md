---
id: otpLogin
title: "OtpLogin 예제 | Refine v5 모범 사례"
display_title: "OTP Login"
sidebar_label: "OTP Login"
description: "Refine v5에서 OtpLogin을 안전하게 구성합니다. 실제 React admin panel을 위한 OAuth, JWT 모범 사례와 code sample을 살펴봅니다."
example-tags: [auth-provider]
---

One-time password(OTP)는 빠르게 만료되고 재사용할 수 없다는 두 가지 핵심 속성을 가진 비밀번호입니다. OTP는 보통 숫자 또는 영숫자 문자열이며 한 번의 login procedure를 위해 생성됩니다. 이 예제는 Refine와 함께 OTP input logic을 활용하는 방법을 보여 줍니다. Refine [AuthProvider](/core/docs/authentication/auth-provider/)를 사용해 one-time password로 애플리케이션에 접근하도록 만들 수 있습니다.

<CodeSandboxExample path="auth-otp" />
