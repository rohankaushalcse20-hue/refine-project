# Интеграция GraphQL для refine

`@refinedev/graphql` предоставляет data provider для GraphQL API. Пакет помогает использовать стандартные CRUD-хуки refine поверх схем GraphQL без написания отдельного слоя состояния и запросов для каждого экрана.

## Установка

```sh
npm install @refinedev/graphql
```

## Базовое использование

Подключите GraphQL endpoint к provider и передайте его в `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/graphql";
```

После настройки можно использовать `useList`, `useOne`, `useCreate`, `useUpdate`, `useDelete` и другие хуки данных refine в привычном формате.

## Документация

- Откройте [документацию GraphQL data provider](https://refine.dev/docs/data/packages/graphql/).
- Общие сведения доступны в [документации по data provider](https://refine.dev/docs/data/data-provider/).
