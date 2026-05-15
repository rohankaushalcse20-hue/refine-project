# Material UI integration for refine

`@refinedev/mui` refine applications में [Material UI](https://mui.com/material-ui/getting-started/) components, layouts, form helpers और data-grid workflows जोड़ता है। यह package refine की headless CRUD architecture को Material Design आधारित UI के साथ जोड़ता है।

## Installation

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Basic usage

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mui";
import CssBaseline from "@mui/material/CssBaseline";

const App = () => (
  <>
    <CssBaseline />
    <Refine>
      <ThemedLayoutV2>{/* routes */}</ThemedLayoutV2>
    </Refine>
  </>
);
```

Material UI tables, forms और layout patterns के साथ admin panels या dashboards बनाते समय यह integration अच्छा fit है।

अधिक जानकारी के लिए [Material UI integration documentation](https://refine.dev/docs/ui-integrations/material-ui/introduction) और [refine tutorial](https://refine.dev/tutorial) देखें।
