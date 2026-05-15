# Integrazione Chakra UI per Refine

`@refinedev/chakra-ui` integra [Chakra UI](https://chakra-ui.com/) con refine e offre componenti e provider UI accessibili per pannelli admin e applicazioni interne.

## Installazione

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Uso di base

Importa i componenti UI da `@refinedev/chakra-ui` e usali insieme al core di refine e al provider Chakra.

```tsx
import { Refine } from "@refinedev/core";
import { notificationProvider, ThemedLayoutV2 } from "@refinedev/chakra-ui";
```

Il pacchetto aiuta a costruire interfacce coerenti con Chakra UI senza cambiare data provider, auth provider o resource di refine.

## Documentazione

- Consulta la [documentazione Chakra UI di refine](https://refine.dev/docs/ui-integrations/chakra-ui/introduction/).
- Per i componenti base, consulta la [documentazione Chakra UI](https://chakra-ui.com/docs/components).
