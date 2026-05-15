# Интеграция Medusa для refine

`@refinedev/medusa` предоставляет data provider для [Medusa](https://medusajs.com/). Пакет помогает строить административные и операционные интерфейсы вокруг commerce-данных Medusa, используя стандартные хуки refine.

## Установка

```sh
npm install @refinedev/medusa
```

## Базовое использование

Импортируйте provider из `@refinedev/medusa`, настройте подключение к Medusa API и передайте provider в `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/medusa";
```

Интеграция полезна для back-office экранов: списков продуктов, заказов, клиентов и других сущностей, которые уже обслуживаются Medusa.

## Документация

- Откройте [документацию Medusa data provider](https://refine.dev/docs/data/packages/medusa/).
- Официальные материалы доступны в [документации Medusa](https://docs.medusajs.com/).
