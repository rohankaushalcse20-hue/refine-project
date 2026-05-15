# Integrazione Medusa per refine

`@refinedev/medusa` collega refine a [Medusa](https://medusajs.com/) per costruire interfacce admin e strumenti operativi sopra backend commerce.

## Installazione

```sh
npm install @refinedev/medusa
```

## Uso di base

Configura il client Medusa e passa il data provider al componente `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/medusa";
```

Il provider permette di usare gli hooks CRUD di refine per gestire risorse commerce come prodotti, ordini e clienti quando sono esposte dal backend Medusa.

## Documentazione

- Consulta la [documentazione dei data provider](https://refine.dev/docs/data/data-provider/).
- Per il backend commerce, consulta la [documentazione Medusa](https://docs.medusajs.com/).
