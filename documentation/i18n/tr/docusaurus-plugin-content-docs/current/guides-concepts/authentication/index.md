---
title: "Authentication | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "Refine'ın login, logout, kullanıcı kimliği ve route korumasını auth provider üzerinden nasıl bağladığını öğrenin."
---

Refine'da authentication `authProvider` ile yönetilir. Bu provider; uygulamanın login, logout, kullanıcı kimliği okuma ve session durumunu kontrol etme davranışlarını tanımlayan fonksiyonları içerir.

## Auth provider

`authProvider`, authentication mantığını tek yerde toplar. Ana UI component'lerini değiştirmeden bunu dahili API'nize, Auth0, Google, Keycloak, NextAuth veya başka identity servislerine bağlayabilirsiniz.

```tsx title=authProvider.ts
export const authProvider = {
  login: async ({ email, password }) => {
    // kendi login endpoint'inizi çağırın
    return { success: true, redirectTo: "/" };
  },
  logout: async () => ({ success: true, redirectTo: "/login" }),
  check: async () => ({ authenticated: true }),
  getIdentity: async () => ({ id: 1, name: "Jane" }),
  onError: async () => ({}),
};
```

## Sayfa koruması

Refine, kullanıcının belirli sayfalara erişip erişemeyeceğini anlamak için `check` metodunu çağırabilir. Session geçerli değilse provider `redirectTo` döndürerek kullanıcıyı login sayfasına yönlendirebilir.

## Kullanıcı kimliği

Header, hesap menüsü, audit logs veya başka component'lere kullanıcı bilgisi sağlamak için `getIdentity` kullanın. Kimlik nesnesinin şekli uygulamanızın ihtiyacına göre belirlenebilir.

## Authentication hataları

`onError`, `401` veya `403` gibi API response'larını ele almayı kolaylaştırır. Bu kalıp sayesinde session sorunlarında logout, token refresh veya redirect davranışları tutarlı uygulanır.
