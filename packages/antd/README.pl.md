# Integracja Ant Design dla Refine

`@refinedev/antd` integruje Refine z [Ant Design](https://ant.design/). Pakiet dodaje gotowe komponenty layoutu, przyciski, formularze, tabele, pola prezentacyjne i hooki dla paneli administracyjnych, dashboardów oraz produktów B2B.

## Instalacja

```sh
npm install @refinedev/antd antd
```

## Podstawowe użycie

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

Integracja zachowuje headlessowe podejście Refine i dodaje prymitywy Ant Design, takie jak `List`, `Create`, `Edit`, `Show`, `useTable` oraz komponenty field.

## Dokumentacja

- Przeczytaj [dokumentację Refine Ant Design](https://refine.dev/docs/ui-integrations/ant-design/introduction).
- Pełny scenariusz znajdziesz w [tutorialu Refine](https://refine.dev/tutorial).
