# Integrazione Material UI per Refine

`@refinedev/mui` integra [Material UI](https://mui.com/material-ui/getting-started/) con refine e fornisce componenti e provider UI per dashboard, pannelli admin e applicazioni B2B.

## Installazione

```sh
npm install @refinedev/mui @mui/material @emotion/react @emotion/styled
```

## Uso di base

Importa i componenti UI da `@refinedev/mui` e usali con il core di refine.

```tsx
import { Refine } from "@refinedev/core";
import { notificationProvider, ThemedLayoutV2 } from "@refinedev/mui";
```

Il pacchetto aggiunge un livello UI Material UI mantenendo invariati resources, providers e hooks di refine.

## Documentazione

- Consulta la [documentazione Material UI di refine](https://refine.dev/docs/ui-integrations/material-ui/introduction/).
- Per i componenti base, consulta la [documentazione Material UI](https://mui.com/material-ui/getting-started/overview/).
