# Интеграция NestJSX CRUD для refine

`@refinedev/nestjsx-crud` предоставляет data provider для RESTful API, построенных с NestJSX CRUD. Он позволяет использовать стандартные CRUD-хуки refine поверх backend API без ручного слоя запросов для каждого ресурса.

## Установка

```sh
npm install @refinedev/nestjsx-crud
```

## Базовое использование

```tsx
import dataProvider from "@refinedev/nestjsx-crud";
```

Передайте `dataProvider("API_URL")` в компонент `Refine`, чтобы подключить ресурсы приложения к NestJSX CRUD API.

## Документация

- Смотрите [пример NestJSX CRUD data provider](https://refine.dev/docs/examples/data-provider/nestjsxCrud/).
- Общие сведения доступны в [документации data provider](https://refine.dev/docs/core/providers/data-provider).
