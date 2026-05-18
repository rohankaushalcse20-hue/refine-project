# Интеграция TanStack React Table для refine

`@refinedev/react-table` связывает хуки данных refine с [TanStack React Table](https://tanstack.com/table/v8). Пакет подходит для headless tables, где разметка и стили остаются под контролем приложения.

## Установка

```sh
npm install @refinedev/react-table @tanstack/react-table
```

## Базовое использование

```tsx
import { useTable } from "@refinedev/react-table";
```

`useTable` принимает конфигурацию колонок TanStack и `refineCoreProps`, чтобы использовать ресурсы, pagination, filters и sorting из refine.

## Документация

- Откройте [документацию TanStack React Table](https://refine.dev/docs/packages/documentation/tanstack-table/introduction)).
- Посмотрите [пример TanStack React Table](https://refine.dev/docs/examples/table/tanstack/advanced-react-table/).
