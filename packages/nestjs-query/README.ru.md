# Интеграция NestJS Query для refine

`@refinedev/nestjs-query` предоставляет data provider для API, построенных с [NestJS Query](https://doug-martin.github.io/nestjs-query/docs). Пакет связывает GraphQL-схему backend-приложения со стандартными CRUD-хуками refine.

## Установка

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## Базовое использование

Настройте GraphQL endpoint и передайте provider в `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/nestjs-query";
```

После подключения ресурсы refine могут работать с фильтрацией, сортировкой, пагинацией и мутациями через API NestJS Query.

## Документация

- Откройте [документацию NestJS Query data provider](https://refine.dev/docs/data/packages/nestjs-query/).
- Подробнее о backend-библиотеке смотрите в [документации NestJS Query](https://doug-martin.github.io/nestjs-query/docs).
