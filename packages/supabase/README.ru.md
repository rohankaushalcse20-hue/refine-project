# Интеграция Supabase для refine

`@refinedev/supabase` предоставляет data provider, live provider и клиентские helpers для приложений refine, которые используют [Supabase](https://supabase.com/).

## Установка

```sh
npm install @refinedev/supabase
```

## Базовое использование

```tsx
import { dataProvider, liveProvider, createClient } from "@refinedev/supabase";
```

Создайте `supabaseClient` через `createClient("SUPABASE_URL", "SUPABASE_KEY")`, затем передайте `dataProvider(supabaseClient)` и `liveProvider(supabaseClient)` в `Refine`.

## Документация

- Смотрите [документацию Supabase data provider](https://refine.dev/docs/packages/documentation/data-providers/supabase/#introduction).
- Посмотрите [пример Supabase data provider](https://refine.dev/docs/examples/data-provider/supabase/).
- Supabase также публикует [tutorial по refine](https://supabase.com/docs/guides/getting-started/tutorials/with-refine).
