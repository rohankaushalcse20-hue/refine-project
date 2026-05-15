# تكامل Material UI مع Refine

تدمج حزمة `@refinedev/mui` بين Refine و[Material UI](https://mui.com/material-ui/getting-started/overview/). وهي تتضمن مكونات وhooks وlayouts لبناء CRUDs ولوحات إدارة وdashboards باستخدام النظام المرئي في MUI.

## التثبيت

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## الاستخدام الأساسي

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

## التوثيق

- راجع [توثيق Refine مع Material UI](https://refine.dev/docs/ui-integrations/material-ui/introduction).
- راجع [دليل Refine الكامل](https://refine.dev/tutorial).
