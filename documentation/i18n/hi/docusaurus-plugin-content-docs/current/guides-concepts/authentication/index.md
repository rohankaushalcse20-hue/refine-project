---
title: "Authentication गाइड | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "Refine applications में authProvider, auth hooks और protected flows को समझने के लिए Hindi summary।"
---

Authentication user की पहचान verify करने की प्रक्रिया है। Refine इसे flexible `authProvider` contract के जरिए संभालता है ताकि आप अपने backend, OAuth flow या session strategy के अनुसार implementation चुन सकें।

## Auth Provider

`authProvider` एक object होता है जिसमें `login`, `logout`, `check`, `getIdentity`, `register`, `forgotPassword` और दूसरे methods शामिल हो सकते हैं।

इसे `<Refine />` को prop के रूप में देने पर Refine के auth hooks उसी provider के methods का उपयोग करते हैं।

```tsx title="App.tsx"
import { Refine, AuthProvider } from "@refinedev/core";

export const authProvider: AuthProvider = {
  login: async ({ email, password }) => {
    const { status } = handleLogin(email, password);

    if (status === 200) {
      return { success: true, redirectTo: "/dashboard" };
    }

    return {
      success: false,
      error: { name: "Login Error", message: "Invalid credentials" },
    };
  },
  check: async () => ({}),
  logout: async () => ({}),
  onError: async () => ({}),
  register: async () => ({}),
  forgotPassword: async () => ({}),
  updatePassword: async () => ({}),
  getPermissions: async () => ({}),
  getIdentity: async () => ({}),
};
```

## उपयोग में आने वाले hooks

- `useLogin`
- `useRegister`
- `useIsAuthenticated`
- `useLogout`
- `useGetIdentity`

ये hooks login, registration, session checks और profile lookup जैसे flows को एक consistent API के साथ expose करते हैं।

## Route protection

`<Authenticated />` component का उपयोग करके आप pages या components को केवल authenticated users तक सीमित कर सकते हैं।

## Data provider के साथ संबंध

Authentication setup होने के बाद credentials को `dataProvider` तक पहुंचाना भी जरूरी होता है, जैसे token headers, cookies या session context। इससे protected APIs के साथ सही requests की जा सकती हैं।
