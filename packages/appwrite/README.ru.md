# Интеграция Appwrite для refine

`@refinedev/appwrite` предоставляет data provider для [Appwrite](https://appwrite.io/). Он связывает стандартные CRUD-хуки refine с коллекциями Appwrite и помогает строить внутренние инструменты поверх существующего backend-проекта.

## Установка

```sh
npm install @refinedev/appwrite
```

## Базовое использование

Импортируйте `dataProvider` из `@refinedev/appwrite`, настройте клиент Appwrite и передайте provider в `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import { dataProvider } from "@refinedev/appwrite";
```

После подключения можно использовать `useList`, `useOne`, `useCreate`, `useUpdate` и другие хуки данных без отдельного слоя запросов в интерфейсе.

## Документация

- Откройте [документацию Appwrite data provider](https://refine.dev/docs/data/packages/appwrite/).
- Справочник Appwrite доступен в [официальной документации](https://appwrite.io/docs).
