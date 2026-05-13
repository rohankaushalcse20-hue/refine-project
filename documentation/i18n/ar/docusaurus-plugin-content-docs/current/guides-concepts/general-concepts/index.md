---
title: "المفاهيم الأساسية | Refine v5"
display_title: "المفاهيم الأساسية"
sidebar_label: "المفاهيم الأساسية"
description: "فهم بنية Refine الـ headless ومفاهيم resources وproviders وhooks وmeta."
---

Refine إطار عمل قابل للتوسعة لبناء تطبيقات الويب بسرعة. يعتمد على **hooks** و**providers** قابلة للتركيب ونمط واضح لإدارة البيانات والحالة.

## مفهوم Headless

Refine لا يفرض عليك مجموعة جاهزة من المكونات ذات التصميم الثابت. هو يوفّر `hooks` و`components` و`providers` وأدوات مساعدة، بينما تبقى طبقة الـ UI تحت سيطرتك.

لهذا تستطيع استخدام Tailwind CSS أو Ant Design أو Material UI أو Mantine أو Chakra UI أو حتى design system خاصاً بك مع الاستمرار في الاستفادة من `@refinedev/core`.

## مفهوم Resource

يمثل **resource** كياناً في التطبيق مثل `products` أو `orders` أو `blogPosts`. تعريف الـ resource يربط المسارات وعمليات CRUD والقوائم والـ providers داخل بنية واحدة.

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

الـ providers هي نقاط التكامل الأساسية في Refine. من خلالها تدير البيانات وauthentication وauthorization وnotifications وi18n وrouting وrealtime وaudit logs.

## Hooks

Hooks Refine headless وغير مرتبطة بمكتبة UI محددة. باستخدام `useGo` و`useCan` و`useTranslate` وغيرها، يمكن التعامل مع التنقل والصلاحيات والترجمة من خلال API موحّد.

## Meta

تُستخدم خاصية `meta` لتمرير معلومات إضافية إلى الـ providers والـ hooks، مثل headers أو معلمات خاصة أو اختيار حقول أو سياق متعدد المستأجرين.
