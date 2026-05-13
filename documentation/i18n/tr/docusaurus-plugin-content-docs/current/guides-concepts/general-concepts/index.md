---
title: "Genel Kavramlar | Refine v5"
display_title: "Genel Kavramlar"
sidebar_label: "Genel Kavramlar"
description: "Refine'ın headless mimarisini ve resources, providers, hooks ile meta kavramlarını anlayın."
---

Refine, web uygulamalarını hızlıca geliştirmek için genişletilebilir bir framework'tür. Temeli, veriyi ve state'i yönetmek için net kalıplar sunan, birlikte kullanılabilir **hooks** ve **providers** yapılarıdır.

## Headless yaklaşım

Refine sizi belirli görünüme sahip bir component setine zorlamaz. `hooks`, `components`, `providers` ve yardımcı araçlar sağlar; UI katmanı ise sizin kontrolünüzde kalır.

Bu sayede `@refinedev/core` ile birlikte Tailwind CSS, Ant Design, Material UI, Mantine, Chakra UI veya kendi design system'inizi kullanabilirsiniz.

## Resource kavramı

**Resource**, uygulamadaki `products`, `orders` veya `blogPosts` gibi varlıkları temsil eder. Resource tanımı route'ları, CRUD işlemlerini, liste sayfalarını ve providers yapılarını tutarlı bir yapıda birbirine bağlar.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        show: "/products/:id",
        edit: "/products/:id/edit",
        create: "/products/new",
      },
    ]}
  />
);
```

## Providers

Providers, Refine içindeki ana entegrasyon noktalarıdır. Uygulama data, authentication, authorization, notifications, i18n, routing, realtime ve audit logs gibi alanları providers üzerinden yönetir.

## Hooks

Refine hooks yapıları headless'tır ve belirli bir UI library'ye bağlı değildir. `useGo`, `useCan`, `useTranslate` ve diğer hooks ile navigasyon, izinler ve çeviriler için ortak bir API kullanabilirsiniz.

## Meta

`meta` özelliği, providers ve hooks yapılarına ek bilgi göndermek için kullanılır; örneğin headers, özel parametreler, field seçimi veya multi-tenant bağlamı.
