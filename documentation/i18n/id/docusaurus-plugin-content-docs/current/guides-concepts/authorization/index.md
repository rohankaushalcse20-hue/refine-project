---
title: "Authorization | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "Pelajari cara Refine memeriksa izin pengguna melalui access control provider."
---

Authorization menentukan apakah pengguna boleh menjalankan action tertentu pada resource tertentu. Di Refine, pemeriksaan ini dilakukan melalui `accessControlProvider`.

## Access control provider

`accessControlProvider` menyediakan metode `can`. Metode ini menerima informasi seperti `resource`, `action`, `params`, dan `id`, lalu mengembalikan apakah action tersebut diizinkan.

```tsx title=accessControlProvider.ts
export const accessControlProvider = {
  can: async ({ resource, action }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Anda tidak dapat menghapus post." };
    }

    return { can: true };
  },
};
```

## Menggunakan `useCan`

Hook `useCan` memudahkan komponen memeriksa izin sebelum menampilkan tombol, link, atau halaman tertentu. Ini membantu UI mengikuti aturan authorization yang sama dengan lapisan aplikasi.

## Resource-aware permissions

Karena izin dikaitkan dengan resource dan action, aturan dapat dibuat granular. Anda dapat mengizinkan `list` tetapi menolak `delete`, atau memberi akses berbeda berdasarkan role, tenant, atau status record.

## Tetap validasi di backend

Pemeriksaan authorization di UI meningkatkan pengalaman pengguna, tetapi backend tetap harus menjadi sumber kebenaran untuk keputusan keamanan.
