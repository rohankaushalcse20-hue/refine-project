---
title: "Forms | Refine v5"
display_title: "Forms"
sidebar_label: "Forms"
description: "Pelajari bagaimana Refine membantu membangun form create dan edit yang terhubung ke data provider."
---

Forms di Refine menghubungkan input pengguna dengan mutasi data. Refine menyediakan hooks dan integrasi UI agar halaman `create` dan `edit` dapat menangani loading, validasi, submit, dan redirect dengan pola yang konsisten.

## Form hooks

Hook seperti `useForm` menyiapkan data awal, submit handler, dan state mutation. Integrasi UI resmi kemudian memetakan hasil hook ini ke komponen form dari Ant Design, Material UI, Mantine, React Hook Form, atau library lain.

```tsx title=CreatePost.tsx
import { useForm } from "@refinedev/react-hook-form";

export const CreatePost = () => {
  const { refineCore, register, handleSubmit } = useForm();

  return (
    <form onSubmit={handleSubmit(refineCore.onFinish)}>
      <input {...register("title")} />
      <button type="submit">Save</button>
    </form>
  );
};
```

## Create dan edit

Pada halaman `create`, form biasanya memanggil `create` di data provider. Pada halaman `edit`, form membaca data record terlebih dahulu lalu memanggil `update` saat submit.

## Mutation mode

Refine mendukung mutation mode seperti `pessimistic`, `optimistic`, dan `undoable`. Pilihan ini menentukan kapan UI diperbarui dan bagaimana pengguna dapat membatalkan perubahan.

## Validasi

Validasi dapat dilakukan dengan library form pilihan Anda atau melalui backend. Refine tidak mengunci strategi validasi, sehingga Anda dapat memakai schema validation, aturan UI framework, atau response error dari API.

## Navigasi setelah submit

Setelah submit berhasil, Refine dapat redirect ke halaman `list`, `show`, `edit`, atau route lain sesuai kebutuhan workflow aplikasi.
