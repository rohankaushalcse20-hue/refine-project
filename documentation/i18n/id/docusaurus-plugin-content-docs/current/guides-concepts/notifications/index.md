---
title: "Notifications | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "Pelajari cara Refine menampilkan feedback sukses dan error melalui notification provider."
---

Notifications memberi feedback cepat kepada pengguna ketika operasi berhasil, gagal, atau membutuhkan perhatian. Refine mengelolanya melalui `notificationProvider`.

## Notification provider

`notificationProvider` biasanya menyediakan metode `open` dan `close`. Integrasi UI resmi memetakan metode ini ke sistem toast atau notification dari UI framework yang Anda gunakan.

```tsx title=notificationProvider.ts
export const notificationProvider = {
  open: ({ message, type }) => {
    console.log(type, message);
  },
  close: (key) => {
    console.log("close", key);
  },
};
```

## Feedback otomatis

Hooks mutasi Refine dapat memicu notifikasi sukses atau error setelah operasi `create`, `update`, atau `delete`. Pesan dapat disesuaikan per hook atau mengikuti konfigurasi provider.

## Pesan yang dapat diterjemahkan

Dalam aplikasi multibahasa, teks notifikasi sebaiknya berasal dari `i18nProvider` atau sistem translation Anda. Dengan begitu, aksi CRUD tetap sama sementara pesan yang terlihat pengguna mengikuti locale aktif.

## Pengalaman pengguna

Gunakan notifikasi untuk feedback singkat. Untuk error yang membutuhkan tindakan, tampilkan juga konteks di halaman atau form agar pengguna tahu cara memperbaikinya.
