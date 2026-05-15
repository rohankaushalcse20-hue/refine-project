# Integrazione Mantine per Refine

`@refinedev/mantine` integra [Mantine](https://mantine.dev/) con refine e offre componenti, layout e provider UI per applicazioni interne.

## Installazione

```sh
npm install @refinedev/mantine @mantine/core @mantine/hooks
```

## Uso di base

Importa i componenti da `@refinedev/mantine` e usali insieme a `@refinedev/core` e al provider Mantine.

```tsx
import { Refine } from "@refinedev/core";
import { notificationProvider, ThemedLayoutV2 } from "@refinedev/mantine";
```

Il pacchetto consente di mantenere data provider, auth provider e routing di refine mentre l'interfaccia segue il design system Mantine.

## Documentazione

- Consulta la [documentazione Mantine di refine](https://refine.dev/docs/ui-integrations/mantine/introduction/).
- Per i componenti base, consulta la [documentazione Mantine](https://mantine.dev/core/package/).
