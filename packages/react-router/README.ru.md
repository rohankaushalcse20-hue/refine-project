# React Router provider для refine

`@refinedev/react-router` подключает refine к [React Router](https://reactrouter.com/). Пакет предоставляет router provider, который синхронизирует ресурсы refine с URL, навигацией и вложенными маршрутами React-приложения.

## Установка

```sh
npm install @refinedev/react-router react-router
```

## Базовое использование

Передайте `routerProvider` в `Refine` и определите маршруты приложения через React Router.

```tsx
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
```

Интеграция помогает использовать навигационные хуки refine, хлебные крошки, меню и resource-based routing без ручного связывания каждого маршрута.

## Документация

- Изучите [документацию router provider](https://refine.dev/docs/core/providers/router-provider/).
- Пример доступен в [React Router example](https://refine.dev/docs/examples/react-router/).
