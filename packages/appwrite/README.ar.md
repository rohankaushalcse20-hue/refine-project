# تكامل Appwrite مع Refine

تربط حزمة `@refinedev/appwrite` تطبيقات Refine بمشاريع [Appwrite](https://appwrite.io/). تتضمن helpers لـ `dataProvider` و`liveProvider` وauthentication حتى يستطيع تطبيق CRUD استخدام Appwrite APIs من دون الارتباط بواجهة محددة.

## التثبيت

```sh
npm install @refinedev/appwrite
```

## الاستخدام الأساسي

```tsx
import { dataProvider, liveProvider } from "@refinedev/appwrite";

const App = () => (
  <Refine
    dataProvider={dataProvider(appwriteClient, {
      databaseId: "DATABASE_ID",
    })}
    liveProvider={liveProvider(appwriteClient, {
      databaseId: "DATABASE_ID",
    })}
  >
    {/* ... */}
  </Refine>
);
```

## التوثيق

راجع [توثيق Refine](https://refine.dev/docs/) لمزيد من التفاصيل حول data providers وrealtime وauthentication.
