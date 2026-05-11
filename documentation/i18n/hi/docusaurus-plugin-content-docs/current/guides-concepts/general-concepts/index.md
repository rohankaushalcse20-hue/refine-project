---
title: "सामान्य अवधारणाएं | Refine v5"
display_title: "सामान्य अवधारणाएं"
sidebar_label: "सामान्य अवधारणाएं"
description: "Refine की headless architecture, resources, providers, hooks और meta concept का परिचय।"
---

Refine एक extensible framework है जो web applications को तेज़ी से बनाने के लिए तैयार किया गया है। इसका design **hooks**, **providers** और reusable data patterns पर आधारित है।

## Headless concept

Refine आपको किसी fixed UI kit में सीमित नहीं करता। यह `hooks`, `components`, `providers` और utilities देता है, जबकि visual layer आपकी पसंद की रहती है।

इसी वजह से आप Tailwind CSS, Ant Design, Material UI, Mantine, Chakra UI या अपने custom components के साथ भी `@refinedev/core` का उपयोग कर सकते हैं।

## Resource concept

Refine में **resource** किसी entity का प्रतिनिधित्व करता है, जैसे `products`, `orders` या `blogPosts`।

Resource definitions routes, CRUD actions, menu entries और provider behavior को एक संरचित रूप देती हैं।

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

## Provider concept

Providers Refine के integration points हैं। यही data access, authentication, authorization, notifications, i18n, routing, realtime और audit जैसी जिम्मेदारियां संभालते हैं।

आप built-in providers इस्तेमाल कर सकते हैं या अपने backend और business rules के हिसाब से custom providers लिख सकते हैं।

## Hook concept

Refine के hooks headless और library-agnostic हैं। उदाहरण के लिए:

- `useGo` अलग-अलग routers के ऊपर navigation को एक जैसा बनाता है।
- `useCan` access control decisions को app में उपलब्ध कराता है।
- `useTranslate` i18n provider के साथ translated text render करता है।

## Meta

`meta` property providers और hooks तक extra context पहुंचाने का तरीका है। यह custom headers, tenant information, field selection या GraphQL query generation जैसी जरूरतों में उपयोगी है।
