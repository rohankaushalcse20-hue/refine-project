---
id: hasura
title: "مثال Hasura | تكامل REST API في Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "طبّق Hasura في Refine v5 وتعلّم الخطوات الأساسية لتوسيع REST وGraphQL لواجهات API مخصصة وتدفقات بيانات قابلة للنمو."
example-tags: [data-provider, live-provider]
---

يمكن دمج أي backend مخصص يعمل عبر REST أو GraphQL مع Refine. يأتي Refine [Hasura](https://hasura.io/) GraphQL Data Provider جاهزاً للاستخدام. بفضل Refine، يمكنك الاتصال بقاعدة بيانات Hasura وإنشاء استعلامات خاصة واستخدام بياناتك بسهولة. يوضح هذا المثال بالتفصيل كيف يمكنك استخدام البيانات الموجودة في قاعدة Hasura داخل مشروع Refine.

## نوع بيانات ID

افتراضياً يفترض data provider أن نوع `ID` هو `uuid`، ويمكنك تغيير هذا السلوك باستخدام خيار `idType`. يمكنك تمرير `Int` أو `uuid` كقيمة لخيار `idType` أو استخدام دالة لتحديد `idType` بناءً على اسم المورد.

#### تمرير 'Int' أو 'uuid' إلى `idType`

يسمح لك هذا بتحديد `idType` لكل الموارد.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### تمرير دالة إلى `idType`

يسمح لك هذا بتحديد `idType` بناءً على اسم المورد.

```tsx
const idTypeMap: Record<string, "Int" | "uuid"> = {
  users: "Int",
  posts: "uuid",
};

const myDataProvider = dataProvider(client, {
  idType: (resource) => idTypeMap[resource] ?? "uuid",
});
```

<CodeSandboxExample path="data-provider-hasura" />
