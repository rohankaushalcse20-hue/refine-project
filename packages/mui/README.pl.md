# Integracja Material UI dla Refine

`@refinedev/mui` integruje Refine z [Material UI](https://mui.com/material-ui/getting-started/). Pakiet dodaje gotowe komponenty layoutu, strony CRUD, przyciski, formularze, tabele i komponenty field oparte na Material UI.

## Instalacja

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Podstawowe użycie

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mui";
import CssBaseline from "@mui/material/CssBaseline";

const App = () => (
  <>
    <CssBaseline />
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </>
);
```

Integracja pomaga szybko zbudować interfejs na Material UI, zachowując logikę data, routing, auth i access-control w Refine.

## Dokumentacja

- Przeczytaj [dokumentację Refine Material UI](https://refine.dev/docs/ui-integrations/material-ui/introduction).
- Pełny scenariusz znajdziesz w [tutorialu Refine](https://refine.dev/tutorial).
