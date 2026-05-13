---
title: "Authentication | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "Pelajari cara Refine menghubungkan login, logout, identitas pengguna, dan proteksi route melalui auth provider."
---

Authentication di Refine dikelola melalui `authProvider`. Provider ini berisi fungsi yang menjelaskan cara aplikasi melakukan login, logout, membaca identitas pengguna, dan memeriksa status sesi.

## Auth provider

`authProvider` menempatkan logika authentication di satu tempat. Anda dapat menghubungkannya ke API internal, Auth0, Google, Keycloak, NextAuth, atau layanan identity lain tanpa mengubah komponen UI utama.

```tsx title=authProvider.ts
export const authProvider = {
  login: async ({ email, password }) => {
    // panggil endpoint login Anda
    return { success: true, redirectTo: "/" };
  },
  logout: async () => ({ success: true, redirectTo: "/login" }),
  check: async () => ({ authenticated: true }),
  getIdentity: async () => ({ id: 1, name: "Jane" }),
  onError: async () => ({}),
};
```

## Proteksi halaman

Refine dapat memanggil `check` untuk menentukan apakah pengguna boleh mengakses halaman tertentu. Jika sesi tidak valid, provider dapat mengembalikan `redirectTo` agar pengguna diarahkan ke halaman login.

## Identitas pengguna

Gunakan `getIdentity` untuk menyediakan informasi pengguna ke header, menu akun, audit logs, atau komponen lain. Bentuk objek identitas dapat mengikuti kebutuhan aplikasi.

## Error authentication

`onError` membantu menangani response API seperti `401` atau `403`. Dengan pola ini, aplikasi dapat melakukan logout, refresh token, atau redirect secara konsisten saat sesi bermasalah.
