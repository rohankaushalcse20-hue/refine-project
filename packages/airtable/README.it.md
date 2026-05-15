# Integrazione Airtable per refine

`@refinedev/airtable` fornisce un data provider per usare [Airtable](https://www.airtable.com/) come backend nelle applicazioni refine.

## Installazione

```sh
npm install @refinedev/airtable
```

## Uso di base

Configura il provider con le credenziali Airtable e passalo al componente `Refine` come `dataProvider`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/airtable";
```

Il provider traduce le operazioni CRUD di refine in richieste verso le basi Airtable, mantenendo invariati resource, hooks e flussi di data fetching.

## Documentazione

- Consulta la [documentazione dei data provider](https://refine.dev/docs/data/data-provider/).
- Per la configurazione del servizio, consulta la [documentazione Airtable](https://airtable.com/developers/web/api/introduction).
