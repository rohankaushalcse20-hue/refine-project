# Интеграция kbar для refine

`@refinedev/kbar` добавляет командную палитру на базе [kbar](https://kbar.vercel.app/) в refine-приложения. Она помогает пользователям быстро переходить между ресурсами и выполнять действия через единый command menu.

## Установка

```sh
npm install @refinedev/kbar
```

## Базовое использование

Подключите provider и UI-компоненты `@refinedev/kbar` вокруг приложения refine.

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";
```

Командная палитра хорошо подходит для административных интерфейсов с большим количеством ресурсов, где быстрый переход важнее глубокой навигации по меню.

## Документация

- Откройте [документацию command palette](https://refine.dev/docs/packages/command-palette/).
- Подробнее о kbar смотрите в [документации kbar](https://kbar.vercel.app/).
