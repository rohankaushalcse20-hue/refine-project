# Integrasi Material UI untuk Refine

Package `@refinedev/mui` menghubungkan Refine dengan [Material UI](https://mui.com/material-ui/getting-started/overview/). Package ini menyertakan komponen, hooks, dan layouts untuk membangun CRUD, admin panel, dan dashboards dengan sistem visual MUI.

## Instalasi

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Penggunaan dasar

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

## Dokumentasi

- Baca [dokumentasi Refine dengan Material UI](https://refine.dev/docs/ui-integrations/material-ui/introduction).
- Baca [tutorial lengkap Refine](https://refine.dev/tutorial).
