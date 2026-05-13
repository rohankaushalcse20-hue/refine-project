---
title: "Notifications | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "Refine'ın başarı ve hata geri bildirimlerini notification provider ile nasıl gösterdiğini öğrenin."
---

Notifications, işlem başarılı olduğunda, başarısız olduğunda veya dikkat gerektirdiğinde kullanıcıya hızlı geri bildirim verir. Refine bunları `notificationProvider` üzerinden yönetir.

## Notification provider

`notificationProvider` genellikle `open` ve `close` metotlarını sağlar. Resmi UI entegrasyonları bu metotları kullandığınız UI framework'ün toast veya notification sistemine bağlar.

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

## Otomatik geri bildirim

Refine mutation hooks, `create`, `update` veya `delete` işlemlerinden sonra başarı ya da hata bildirimleri tetikleyebilir. Mesajlar her hook için özelleştirilebilir veya provider yapılandırmasını izleyebilir.

## Çevrilebilir mesajlar

Çok dilli uygulamalarda notification metinleri `i18nProvider` veya kendi translation sisteminizden gelmelidir. Böylece CRUD action'ları aynı kalırken kullanıcıya görünen mesaj aktif locale'e uyar.

## Kullanıcı deneyimi

Notifications kısa geri bildirimler için kullanılmalıdır. Aksiyon gerektiren hatalarda, kullanıcının nasıl düzelteceğini anlaması için sayfa veya form içinde de bağlam gösterin.
