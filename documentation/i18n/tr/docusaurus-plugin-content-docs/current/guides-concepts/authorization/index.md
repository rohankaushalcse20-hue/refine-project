---
title: "Authorization | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "Refine'ın kullanıcı izinlerini access control provider ile nasıl kontrol ettiğini öğrenin."
---

Authorization, kullanıcının belirli bir resource üzerinde belirli bir action çalıştırıp çalıştıramayacağını belirler. Refine'da bu kontrol `accessControlProvider` üzerinden yapılır.

## Access control provider

`accessControlProvider`, `can` metodunu sağlar. Bu metot `resource`, `action`, `params` ve `id` gibi bilgileri alır, ardından action'ın izinli olup olmadığını döndürür.

```tsx title=accessControlProvider.ts
export const accessControlProvider = {
  can: async ({ resource, action }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Post silemezsiniz." };
    }

    return { can: true };
  },
};
```

## `useCan` kullanma

`useCan` hook'u, component'lerin buton, link veya belirli bir sayfayı göstermeden önce izin kontrolü yapmasını kolaylaştırır. Böylece UI, uygulama katmanındaki authorization kurallarıyla aynı çizgide kalır.

## Resource-aware permissions

İzinler resource ve action ile ilişkilendirildiği için kurallar ayrıntılı kurulabilir. `list` izni verip `delete` iznini reddedebilir ya da role, tenant veya record durumuna göre farklı erişimler tanımlayabilirsiniz.

## Backend doğrulaması sürmeli

UI tarafındaki authorization kontrolleri kullanıcı deneyimini iyileştirir; güvenlik kararları için backend yine de doğruluk kaynağı olmalıdır.
