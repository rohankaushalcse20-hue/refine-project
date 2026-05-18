# Интеграция Strapi для refine

`@refinedev/strapi` предоставляет data provider и auth helper для проектов refine, использующих [Strapi](https://strapi.io/) как headless CMS.

## Установка

```sh
npm install @refinedev/strapi axios
```

## Базовое использование

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi";
```

Передайте `DataProvider("API_URL", axiosInstance)` в `Refine`, чтобы работать с ресурсами Strapi через стандартные CRUD-хуки refine.

## Документация

- Посмотрите [пример Strapi data provider](https://refine.dev/docs/examples/data-provider/strapi/).
- Общая справка доступна в [документации data provider](https://refine.dev/docs/core/providers/data-provider).
