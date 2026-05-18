---
id: otpLogin
title: "OtpLogin example | Refine v5 में best practices"
display_title: "OTP Login"
sidebar_label: "OTP Login"
description: "Refine v5 में OTP Login सुरक्षित करें। OAuth, JWT और one-time password flow को Hindi में समझें।"
example-tags: [auth-provider]
---

One-time password (OTP) ऐसा password होता है जिसमें दो मूल properties होती हैं: यह जल्दी expire हो जाता है और इसे दोबारा इस्तेमाल नहीं किया जा सकता। OTPs आम तौर पर numeric या alphanumeric strings होते हैं और एक single login procedure के लिए generate किए जाते हैं। यह example दिखाता है कि Refine के साथ OTP input logic कैसे उपयोग किया जा सकता है। आप Refine [AuthProvider](/core/docs/authentication/auth-provider/) के साथ अपने application में access देने के लिए one-time passwords इस्तेमाल कर सकते हैं।

<CodeSandboxExample path="auth-otp" />
