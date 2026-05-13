---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Refine'ın resources, route actions ve router provider arasında nasıl bağlantı kurduğunu öğrenin."
---

Refine kendi router'ını getirmez. Bunun yerine `routerProvider` üzerinden router ile konuşur; böylece uygulama React Router, Next.js, Remix veya başka routing entegrasyonlarını kullanabilir.

## Router provider

`routerProvider`, Refine'a mevcut konumu okuma, link üretme ve navigasyon çalıştırma yolu sağlar. `@refinedev/react-router` gibi resmi entegrasyonlar uygun implementasyonu hazır olarak sunar.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";

export const App = () => (
  <Refine
    routerProvider={routerProvider}
    resources={[
      {
        name: "posts",
        list: "/posts",
        create: "/posts/create",
        edit: "/posts/edit/:id",
        show: "/posts/show/:id",
      },
    ]}
  />
);
```

## Route actions

Her resource, `list`, `create`, `edit` ve `show` gibi action'lar için route tanımlayabilir. Refine bu metadata ile navigasyon, breadcrumbs, action buttons ve redirect davranışlarını tutarlı üretir.

## Programatik navigasyon

Uygulama kodundan sayfa değiştirmek gerektiğinde `useGo`, `useBack` ve `useGetToPath` gibi hooks kullanın. Bu hooks, navigasyonu aktif resource ve router ile uyumlu tutar.

## URL'leri açık tutma

Refine, resource URL'leri açık yazıldığında en iyi şekilde çalışır. Bu yaklaşım menüleri, permissions kurallarını ve deep links yapılarını ekip için daha anlaşılır, uygulama büyüdükçe de daha güvenli hale getirir.
