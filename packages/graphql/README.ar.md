# GraphQL data provider

توفر حزمة `@refinedev/graphql` مزود بيانات لربط مشاريع Refine بـ backends مخصصة تعتمد على GraphQL. وهي قاعدة مرنة عندما تريد تعريف queries وmutations وقواعد النقل الخاصة بك.

## التثبيت

```sh
npm install @refinedev/graphql
```

## الاستخدام الأساسي

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => {
  return (
    <Refine dataProvider={dataProvider(client)}>
      {/* ... */}
    </Refine>
  );
};
```

## متى تستخدمها؟

استخدمها عندما يوفّر الـ backend لديك endpoint بنمط GraphQL وتحتاج إلى تكييف طبقة بيانات Refine مع types وresources وقواعد الاستعلام في مشروعك.

## المزيد

راجع توثيق GraphQL data provider في Refine لتوسيع التكامل.
