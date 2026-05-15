# Next.js router provider для refine

`@refinedev/nextjs-router` подключает refine к маршрутизации Next.js. Пакет предоставляет router provider, который помогает ресурсам refine синхронизироваться с URL, навигацией и страницами Next.js-приложения.

## Установка

```sh
npm install @refinedev/nextjs-router
```

## Базовое использование

Импортируйте router provider и передайте его в `Refine` вместе с остальными provider-ами приложения.

```tsx
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/nextjs-router";
```

Интеграция полезна для проектов, где refine-экраны должны жить внутри Next.js и использовать его модель страниц, layout-ов и навигации.

## Документация

- Изучите [документацию router provider](https://refine.dev/docs/core/providers/router-provider/).
- Для Next.js примеров откройте [раздел examples](https://refine.dev/docs/examples/next-js/next-js/).
