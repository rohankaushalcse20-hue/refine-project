# Интеграция Strapi v4 для refine

`@refinedev/strapi-v4` предоставляет data provider и auth helper для Strapi v4. Пакет помогает использовать resources, CRUD hooks и auth flows refine поверх API Strapi v4.

## Установка

```sh
npm install @refinedev/strapi-v4 axios
```

## Базовое использование

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi-v4";
```

Настройте `axiosInstance`, передайте `DataProvider("API_URL", axiosInstance)` в `Refine` и используйте хуки данных refine как обычно.

## Документация

- Откройте [документацию Strapi v4 data provider](https://refine.dev/docs/packages/documentation/data-providers/strapi-v4/).
- Посмотрите [пример Strapi v4 data provider](https://refine.dev/docs/examples/data-provider/strapi-v4/).
