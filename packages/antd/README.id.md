# Integrasi Ant Design untuk Refine

Package `@refinedev/antd` menghubungkan Refine dengan [Ant Design](https://ant.design/). Package ini menyediakan komponen, hooks, dan layouts siap pakai untuk membangun admin panel, dashboards, dan aplikasi B2B dengan pengalaman visual yang konsisten.

## Instalasi

```sh
npm install @refinedev/antd antd
```

## Penggunaan dasar

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

Package ini mempertahankan logika Refine yang headless dan menambahkan primitives Ant Design seperti `List`, `Create`, `Edit`, `Show`, `useTable`, serta field tampilan.

## Dokumentasi

- Baca [dokumentasi Refine dengan Ant Design](https://refine.dev/docs/ui-integrations/ant-design/introduction).
- Baca [tutorial lengkap Refine](https://refine.dev/tutorial).
