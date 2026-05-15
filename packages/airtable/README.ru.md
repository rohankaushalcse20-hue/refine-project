# Интеграция Airtable для refine

`@refinedev/airtable` предоставляет data provider для работы refine с [Airtable](https://www.airtable.com/). Он позволяет использовать базы Airtable как источник данных для CRUD-экранов, админ-панелей и внутренних инструментов.

## Установка

```sh
npm install @refinedev/airtable
```

## Базовое использование

Подключите provider к `Refine` и передайте параметры доступа к Airtable. Refine продолжит использовать стандартные хуки данных, такие как `useList`, `useOne`, `useCreate`, `useUpdate` и `useDelete`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/airtable";
```

Пакет подходит для быстрых административных интерфейсов поверх таблиц Airtable без написания отдельного REST API.

## Документация

- Откройте [документацию Airtable data provider](https://refine.dev/docs/data/packages/airtable/).
- Общие сведения доступны в [документации по data provider](https://refine.dev/docs/data/data-provider/).
