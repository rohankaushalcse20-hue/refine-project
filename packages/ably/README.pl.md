# Integracja Ably dla Refine

`@refinedev/ably` podłącza [Ably](https://ably.com/) jako live provider dla aplikacji Refine. Pakiet pomaga dostarczać aktualizacje w czasie rzeczywistym przez model publish/subscribe oraz połączenia WebSocket.

## Instalacja

```sh
npm install @refinedev/ably
```

## Podstawowe użycie

Zaimportuj `liveProvider` z `@refinedev/ably`, przekaż skonfigurowanego klienta Ably i podłącz provider do komponentu `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import { liveProvider } from "@refinedev/ably";
```

Ten provider jest przydatny, gdy listy, tabele i strony szczegółów mają reagować na zdarzenia tworzenia, aktualizacji i usuwania bez ręcznego odświeżania interfejsu.

## Dokumentacja

- Przeczytaj [dokumentację live provider](https://refine.dev/docs/realtime/live-provider/).
- Więcej informacji o platformie znajdziesz w [dokumentacji Ably](https://ably.com/docs).
