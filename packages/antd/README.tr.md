# Refine icin Ant Design entegrasyonu

`@refinedev/antd`, Refine'i [Ant Design](https://ant.design/) ile entegre eder. Admin panel, dashboard ve B2B uygulamalarinda tutarli bir Ant Design deneyimi olusturmak icin hazir layout'lar, component'ler ve hook'lar sunar.

## Kurulum

```sh
npm install @refinedev/antd antd
```

## Temel kullanim

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

Package, Refine'in headless is mantigini korurken `List`, `Create`, `Edit`, `Show`, `useTable` ve field component'leri gibi Ant Design tabanli arayuz primitifleri saglar.

## Dokumantasyon

- [Refine Ant Design dokumantasyonunu](https://refine.dev/docs/ui-integrations/ant-design/introduction) inceleyin.
- Uctan uca ornekler icin [Refine tutorial'ini](https://refine.dev/tutorial) takip edin.
