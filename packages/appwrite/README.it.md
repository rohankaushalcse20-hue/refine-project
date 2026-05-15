# Integrazione Appwrite per refine

`@refinedev/appwrite` collega [Appwrite](https://appwrite.io/) a refine per usare database, autenticazione e servizi backend Appwrite nelle applicazioni React.

## Installazione

```sh
npm install @refinedev/appwrite appwrite
```

## Uso di base

Configura il client Appwrite e passa i provider esportati dal pacchetto a `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import { dataProvider, liveProvider } from "@refinedev/appwrite";
```

Il pacchetto consente di mantenere le API refine per resources e hooks mentre le richieste vengono eseguite contro il progetto Appwrite configurato.

## Documentazione

- Consulta la [documentazione del provider Appwrite](https://refine.dev/docs/data/packages/appwrite/).
- Per endpoint, database e autenticazione, consulta la [documentazione Appwrite](https://appwrite.io/docs).
