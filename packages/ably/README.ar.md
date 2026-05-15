# تكامل Ably مع Refine

توفر حزمة `@refinedev/ably` مزود `liveProvider` مبنياً على [Ably](https://ably.com/) لتطبيقات Refine. استخدمها عندما تحتاج أداة داخلية أو dashboard أو لوحة إدارة إلى تحديثات فورية عبر WebSocket.

## التثبيت

```sh
npm install @refinedev/ably
```

## الاستخدام الأساسي

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => (
  <Refine liveProvider={liveProvider(ablyClient)}>
    {/* ... */}
  </Refine>
);
```

يربط الـ provider أحداث Ably بعقد realtime في Refine، مع إبقاء منطق البيانات منفصلاً عن طبقة الواجهة.

## التوثيق

- راجع [توثيق live provider في Refine](https://refine.dev/docs/api-references/providers/live-provider/).
- راجع أيضاً [دليل Ably الرسمي مع Refine](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine).
