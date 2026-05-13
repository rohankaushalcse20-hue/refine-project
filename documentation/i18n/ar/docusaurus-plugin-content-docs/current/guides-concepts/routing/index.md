---
title: "التوجيه | Refine v5"
display_title: "التوجيه"
sidebar_label: "التوجيه"
description: "تعرّف على دمج React Router وNext.js وRemix مع نظام routing في Refine."
---

التوجيه عنصر أساسي في أي تطبيق CRUD. وبما أن Refine يعتمد على بنية headless، فهو لا يقيّدك بإطار توجيه واحد، بل يترك لك اختيار الحل المناسب للمشروع.

يوفر Refine تكاملاً جاهزاً مع **React Router** و**Next.js** و**Remix**، مع مزايا مثل استنتاج المعلمات، وإعادة التوجيه بعد العمليات، وأدوات navigation وbreadcrumbs.

## إضافة routerProvider

استورد حزمة التوجيه المناسبة ثم مرّرها إلى `<Refine />` عبر الخاصية `routerProvider`.

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Routes } from "react-router";

export const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* Your route definitions */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

## ملاحظات عملية

- احرص على أن يبقى الربط واضحاً بين `resources` وroutes.
- دع الـ router يمرر `resource` و`id` وبقية المعلمات تلقائياً إلى الـ hooks قدر الإمكان.
- تذكّر أن Refine router-agnostic، لذلك تبقى شجرة المسارات الفعلية مسؤولية التطبيق نفسه.
