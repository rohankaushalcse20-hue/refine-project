# Интеграция Ant Design для Refine

`@refinedev/antd` интегрирует Refine с [Ant Design](https://ant.design/). Пакет добавляет готовые layout-компоненты, кнопки, формы, таблицы, поля отображения и хуки для административных интерфейсов, dashboard-приложений и B2B-продуктов.

## Установка

```sh
npm install @refinedev/antd antd
```

## Базовое использование

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

Интеграция сохраняет headless-подход Refine и добавляет Ant Design-примитивы вроде `List`, `Create`, `Edit`, `Show`, `useTable` и field-компонентов.

## Документация

- Изучите [документацию Refine Ant Design](https://refine.dev/docs/ui-integrations/ant-design/introduction).
- Для полного сценария пройдите [tutorial Refine](https://refine.dev/tutorial).
