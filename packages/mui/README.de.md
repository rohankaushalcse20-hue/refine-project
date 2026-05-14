# Material UI integration for Refine

`@refinedev/mui` stellt Refine-Komponenten, Layouts und Hooks fuer [Material UI](https://mui.com/material-ui/getting-started/) bereit. Es verbindet Material UI Tabellen, Formulare und Layouts mit Refines Daten-, Routing- und Ressourcenmodell.

## Installation

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Schnellstart

```tsx
import React from "react";
import { Refine, useMany } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mui";
import dataProvider from "@refinedev/simple-rest";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";

import CssBaseline from "@mui/material/CssBaseline";

export default function App() {
  return (
    <BrowserRouter>
      <CssBaseline />
      <Refine
        dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
        routerProvider={routerProvider}
        resources={[
          {
            name: "products",
            list: "/products",
          },
        ]}
      >
        <Routes>
          <Route
            element={
              <ThemedLayoutV2>
                <Outlet />
              </ThemedLayoutV2>
            }
          >
            <Route path="/products">
              <Route index element={<ProductList />} />
            </Route>
          </Route>
        </Routes>
      </Refine>
    </BrowserRouter>
  );
}
```

Nutze dieses package, wenn du Refine-Anwendungen mit Material UI, MUI X Data Grid und einer anpassbaren Enterprise-Oberflaeche bauen moechtest.

Weitere Details findest du in der [Refine documentation](https://refine.dev/docs/) und in den [tutorials](https://refine.dev/docs/tutorial/introduction/index/).
