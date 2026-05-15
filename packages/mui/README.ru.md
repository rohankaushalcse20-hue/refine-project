# Интеграция Material UI для Refine

`@refinedev/mui` интегрирует Refine с [Material UI](https://mui.com/material-ui/getting-started/). Пакет добавляет готовые layout-компоненты, страницы CRUD, кнопки, формы, таблицы и field-компоненты на базе Material UI.

## Установка

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Базовое использование

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mui";
import CssBaseline from "@mui/material/CssBaseline";

const App = () => (
  <>
    <CssBaseline />
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </>
);
```

Интеграция помогает быстро собрать интерфейс на Material UI, сохраняя data, routing, auth и access-control логику в Refine.

## Документация

- Изучите [документацию Refine Material UI](https://refine.dev/docs/ui-integrations/material-ui/introduction).
- Для полного сценария пройдите [tutorial Refine](https://refine.dev/tutorial).
