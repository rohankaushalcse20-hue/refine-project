# Integrazione Ably per refine

`@refinedev/ably` collega [Ably](https://ably.com/) come live provider per le applicazioni refine. Il pacchetto aiuta a distribuire aggiornamenti in tempo reale tramite il modello publish/subscribe e connessioni WebSocket.

## Installazione

```sh
npm install @refinedev/ably
```

## Uso di base

Importa `liveProvider` da `@refinedev/ably`, passa un client Ably configurato e collega il provider al componente `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import { liveProvider } from "@refinedev/ably";
```

Questo provider è utile quando liste, tabelle e pagine di dettaglio devono reagire a eventi di creazione, aggiornamento ed eliminazione senza aggiornare manualmente l'interfaccia.

## Documentazione

- Consulta la [documentazione del live provider](https://refine.dev/docs/realtime/live-provider/).
- Per i dettagli sulla piattaforma, consulta la [documentazione di Ably](https://ably.com/docs).
