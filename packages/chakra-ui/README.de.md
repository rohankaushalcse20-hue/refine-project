# Chakra UI integration for Refine

`@refinedev/chakra-ui` stellt Refine-kompatible Layouts, Theme-Hilfen und UI-Bausteine fuer [Chakra UI](https://chakra-ui.com/) bereit. Es verbindet Chakra UI Komponenten mit Refines Ressourcen-, Benachrichtigungs- und Formular-Workflows.

## Installation

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Schnellstart

```tsx
import React from "react";
import { Refine } from "@refinedev/core";
import {
  ErrorComponent,
  ThemedLayoutV2,
  RefineThemes,
  useNotificationProvider,
} from "@refinedev/chakra-ui";
import dataProvider from "@refinedev/simple-rest";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";

export default function App() {
  return (
    <BrowserRouter>
      <ChakraProvider theme={RefineThemes.Blue}>
        <Refine
          routerProvider={routerProvider}
          dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
          notificationProvider={useNotificationProvider()}
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
              <Route path="*" element={<ErrorComponent />} />
            </Route>
          </Routes>
        </Refine>
      </ChakraProvider>
    </BrowserRouter>
  );
}
```

Dieses package ist passend, wenn Barrierefreiheit, Theme-Anpassung und Chakra UI Komponenten zentrale Anforderungen deiner Refine-Oberflaeche sind.

Weitere Details findest du in der [Refine documentation](https://refine.dev/docs/) und in den [tutorials](https://refine.dev/docs/tutorial/introduction/index/).
