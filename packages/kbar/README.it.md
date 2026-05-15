# Integrazione kbar per refine

`@refinedev/kbar` integra [kbar](https://kbar.vercel.app/) con refine per aggiungere una command palette navigabile da tastiera.

## Installazione

```sh
npm install @refinedev/kbar kbar
```

## Uso di base

Avvolgi l'applicazione con i provider necessari e usa le azioni generate dalle resources refine.

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";
```

La palette aiuta gli utenti a raggiungere rapidamente pagine, azioni e resources senza aggiungere logica di navigazione duplicata.

## Documentazione

- Consulta la [documentazione kbar di refine](https://refine.dev/docs/packages/kbar/).
- Per l'API della command palette, consulta la [documentazione kbar](https://kbar.vercel.app/docs).
