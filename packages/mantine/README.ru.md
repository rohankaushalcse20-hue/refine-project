# Интеграция Mantine для Refine

`@refinedev/mantine` интегрирует Refine с [Mantine](https://mantine.dev/). Пакет добавляет готовые layout-компоненты, кнопки, формы, уведомления, таблицы и field-компоненты для приложений на Mantine.

## Установка

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## Базовое использование

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mantine";
import { MantineProvider } from "@mantine/core";

const App = () => (
  <MantineProvider>
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </MantineProvider>
);
```

Интеграция сохраняет headless-архитектуру Refine и предоставляет Mantine-реализации для типовых CRUD-экранов.

## Документация

- Изучите [документацию Refine Mantine](https://refine.dev/docs/ui-integrations/mantine/introduction).
- Для полного сценария пройдите [tutorial Refine](https://refine.dev/tutorial).
