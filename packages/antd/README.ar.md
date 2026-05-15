# تكامل Ant Design مع Refine

تدمج حزمة `@refinedev/antd` بين Refine و[Ant Design](https://ant.design/). وهي توفر مكونات وhooks وlayouts جاهزة لبناء لوحات إدارة وdashboards وتطبيقات B2B بتجربة مرئية متسقة.

## التثبيت

```sh
npm install @refinedev/antd antd
```

## الاستخدام الأساسي

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/antd";

import "antd/dist/reset.css";

const App = () => (
  <Refine>
    <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
  </Refine>
);
```

تحافظ الحزمة على منطق Refine الـ headless وتضيف primitives من Ant Design مثل `List` و`Create` و`Edit` و`Show` و`useTable` وحقول العرض.

## التوثيق

- راجع [توثيق Refine مع Ant Design](https://refine.dev/docs/ui-integrations/ant-design/introduction).
- راجع [دليل Refine الكامل](https://refine.dev/tutorial).
