# تكامل Hasura

تربط حزمة `@refinedev/hasura` بين Refine ومشاريع Hasura، وتبسّط استخدام GraphQL في تطبيقات CRUD. وهي خيار جيد عندما تريد العمل مع queries وmutations وsubscriptions من قاعدة منسجمة مع منظومة Hasura.

## التثبيت

```sh
npm install @refinedev/hasura
```

## الاستخدام الأساسي

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("HASURA_API_URL", {
  headers: {
    "x-hasura-role": "public",
  },
});

const App = () => {
  return (
    <Refine dataProvider={dataProvider(client)}>
      {/* ... */}
    </Refine>
  );
};
```

## متى تستخدمها؟

استخدمها عندما يعتمد مشروعك على Hasura لتقديم GraphQL أو إدارة roles أو إضافة قدرات realtime عبر تكامل جاهز.

## المزيد

راجع توثيق Refine الخاص بـ data providers ودليل Hasura لتكييف التكامل مع schema مشروعك.
