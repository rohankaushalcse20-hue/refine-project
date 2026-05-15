# Integracion de Material UI para Refine

`@refinedev/mui` integra Refine con [Material UI](https://mui.com/material-ui/getting-started/overview/). Incluye componentes, hooks y layouts para crear CRUDs, paneles administrativos y dashboards con el sistema visual de MUI.

## Instalacion

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Uso basico

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mui";
import CssBaseline from "@mui/material/CssBaseline";
import GlobalStyles from "@mui/material/GlobalStyles";

const App = () => (
  <>
    <CssBaseline />
    <GlobalStyles styles={{ html: { WebkitFontSmoothing: "auto" } }} />
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </>
);
```

## Documentacion

- Consulta la [documentacion de Refine con Material UI](https://refine.dev/docs/ui-integrations/material-ui/introduction).
- Revisa el [tutorial completo de Refine](https://refine.dev/tutorial).
