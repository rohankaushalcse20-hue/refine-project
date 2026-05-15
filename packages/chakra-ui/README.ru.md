# Интеграция Chakra UI для Refine

`@refinedev/chakra-ui` подключает Refine к [Chakra UI](https://chakra-ui.com/). Пакет добавляет готовые компоненты, layout-структуры, формы, кнопки и field-компоненты для приложений, которым нужен доступный и модульный интерфейс.

## Установка

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Базовое использование

```tsx
import { Refine } from "@refinedev/core";
import { RefineThemes, ThemedLayoutV2 } from "@refinedev/chakra-ui";
import { ChakraProvider } from "@chakra-ui/react";

const App = () => (
  <ChakraProvider theme={RefineThemes.Blue}>
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </ChakraProvider>
);
```

Интеграция оставляет бизнес-логику в Refine и предоставляет Chakra UI-компоненты для списков, страниц создания, редактирования и просмотра.

## Документация

- Изучите [документацию Refine Chakra UI](https://refine.dev/docs/ui-integrations/chakra-ui/introduction).
- Для полного сценария пройдите [tutorial Refine](https://refine.dev/tutorial).
