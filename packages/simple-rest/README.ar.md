# Simple REST data provider

`@refinedev/simple-rest` هو data provider موجّه إلى REST APIs ذات البنية الواضحة. وهو مناسب عندما تريد ربط `resources` في Refine بـ HTTP endpoints مباشرةً.

## التثبيت

```sh
npm install @refinedev/simple-rest
```

## الاستخدام الأساسي

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

يكون هذا الـ provider مناسباً عندما يوفّر الـ backend endpoints قياسية لعمليات list وcreate وupdate وdelete. وإذا احتجت إلى headers أو params خاصة، فيمكنك تغليفه وتوسيعه بسهولة.
