# Refine codemod

Package `@refinedev/codemod` berisi transformations untuk memperbarui project Refine antarversi dan menerapkan perubahan API yang mekanis dengan pekerjaan manual yang lebih sedikit.

## Instalasi dan penggunaan

Jalankan codemod dari root project Anda dan selalu tinjau diff yang dihasilkan sebelum menyimpan perubahan:

```sh
npx @refinedev/codemod
```

## Kapan digunakan?

Gunakan package ini saat migrations atau update besar, terutama ketika versi Refine mengubah imports, nama package, atau pola yang muncul berulang di banyak file.

## Dokumentasi

Baca [dokumentasi utama Refine](https://refine.dev/docs/) dan catatan migration yang sesuai sebelum menjalankan transformations pada branch bersama.
