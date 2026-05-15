# Интеграция Hasura для refine

`@refinedev/hasura` подключает refine к [Hasura](https://hasura.io/) через GraphQL API. Пакет помогает быстро строить CRUD-интерфейсы поверх данных, которые Hasura публикует с учетом схемы и правил доступа.

## Установка

```sh
npm install @refinedev/hasura
```

## Базовое использование

Импортируйте `dataProvider` из `@refinedev/hasura`, настройте endpoint Hasura и передайте provider в `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/hasura";
```

Интеграция подходит для приложений, где backend уже описан в Hasura, а интерфейсу нужны списки, формы и страницы просмотра на основе ресурсов refine.

## Документация

- Изучите [документацию Hasura data provider](https://refine.dev/docs/data/packages/hasura/).
- Официальные материалы доступны в [документации Hasura](https://hasura.io/docs/).
