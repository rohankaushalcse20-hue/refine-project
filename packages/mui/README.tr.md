# Refine icin Material UI entegrasyonu

`@refinedev/mui`, Refine'i [Material UI](https://mui.com/material-ui/getting-started/overview/) ile entegre eder. CRUD ekranlari, admin panelleri ve dashboard'lar icin MUI tabanli component'ler, hook'lar ve layout'lar saglar.

## Kurulum

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Temel kullanim

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

## Dokumantasyon

- [Refine Material UI dokumantasyonunu](https://refine.dev/docs/ui-integrations/material-ui/introduction) inceleyin.
- Uctan uca kurulumlar icin [Refine tutorial'ini](https://refine.dev/tutorial) takip edin.
