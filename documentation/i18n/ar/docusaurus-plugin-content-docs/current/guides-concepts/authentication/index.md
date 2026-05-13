---
title: "المصادقة | Refine v5"
display_title: "المصادقة"
sidebar_label: "المصادقة"
description: "استخدم auth provider في Refine لإدارة login وlogout والتحقق من الجلسة."
---

المصادقة هي ما يثبت هوية المستخدم أو العميل. في Refine، يتم ذلك عبر `authProvider` مرن يمكن وصله بأي backend أو OAuth flow أو strategy خاصة بالجلسات.

## Auth provider

عادةً ما يضم `authProvider` عمليات login وlogout وcheck والاستعلام عن identity أو permissions، بالإضافة إلى معالجة الأخطاء.

```tsx title="auth-provider.ts"
import { AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  login: async ({ email, password }) => {
    const isValid = email && password;
    return isValid
      ? { success: true, redirectTo: "/dashboard" }
      : {
          success: false,
          error: { name: "LoginError", message: "Invalid credentials" },
        };
  },
  check: async () => ({ authenticated: true }),
  logout: async () => ({ success: true, redirectTo: "/login" }),
  onError: async () => ({}),
};
```

## Hooks المصادقة

يوفر Refine hooks مثل `useLogin` و`useLogout` و`useRegister` و`useIsAuthenticated` و`useGetIdentity`. كما يمكنك استخدام `<Authenticated />` لحماية الصفحات أو لإظهار محتوى مختلف بحسب حالة الجلسة.

## أسلوب الدمج

يمكنك تنفيذ منطق المصادقة بنفسك أو دمج موفري هوية مثل Google أو Auth0 أو Amazon Cognito أو Okta، بشرط أن يلتزم `authProvider` بالعقدة المتوقعة.
