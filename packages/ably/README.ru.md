# Интеграция Ably для refine

`@refinedev/ably` подключает [Ably](https://ably.com/) как live provider для refine-приложений. Пакет помогает доставлять обновления в реальном времени через модель publish/subscribe и WebSocket-соединения.

## Установка

```sh
npm install @refinedev/ably
```

## Базовое использование

Импортируйте `liveProvider` из `@refinedev/ably`, передайте настроенный клиент Ably и подключите provider к компоненту `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import { liveProvider } from "@refinedev/ably";
```

Такой provider полезен, когда списки, таблицы и подробные страницы должны реагировать на события создания, обновления и удаления без ручного обновления интерфейса.

## Документация

- Изучите [документацию live provider](https://refine.dev/docs/realtime/live-provider/).
- Подробнее о платформе смотрите в [документации Ably](https://ably.com/docs).
