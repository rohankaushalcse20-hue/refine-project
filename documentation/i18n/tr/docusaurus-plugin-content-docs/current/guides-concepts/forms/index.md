---
title: "Forms | Refine v5"
display_title: "Forms"
sidebar_label: "Forms"
description: "Refine'ın data provider'a bağlı create ve edit formları oluşturmaya nasıl yardımcı olduğunu öğrenin."
---

Refine'da forms, kullanıcı input'larını data mutations ile bağlar. Refine, `create` ve `edit` sayfalarının loading, validation, submit ve redirect süreçlerini tutarlı bir kalıpla yönetmesi için hooks ve UI entegrasyonları sağlar.

## Form hooks

`useForm` gibi hooks başlangıç verisini, submit handler'ı ve mutation state'ini hazırlar. Resmi UI entegrasyonları, bu hook sonucunu Ant Design, Material UI, Mantine, React Hook Form veya başka library'lerin form component'lerine bağlar.

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

## Create ve edit

`create` sayfasında form genellikle data provider'daki `create` metodunu çağırır. `edit` sayfasında önce kayıt verisi okunur, submit sırasında `update` çalıştırılır.

## Mutation mode

Refine `pessimistic`, `optimistic` ve `undoable` gibi mutation mode seçeneklerini destekler. Bu seçim, UI'ın ne zaman güncelleneceğini ve kullanıcının değişikliği nasıl geri alabileceğini belirler.

## Validation

Validation, tercih ettiğiniz form library ile veya backend üzerinden yapılabilir. Refine validation stratejisini kilitlemez; schema validation, UI framework kuralları veya API'den dönen hata response'ları kullanılabilir.

## Submit sonrası navigasyon

Submit başarılı olduğunda Refine ihtiyaca göre `list`, `show`, `edit` veya başka bir route'a redirect yapabilir.
