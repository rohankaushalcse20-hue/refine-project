# Mantine UI integration for Refine

`@refinedev/mantine` stellt Refine-Komponenten und Provider fuer [Mantine](https://mantine.dev/) bereit. Es kombiniert Mantine UI, notifications und form utilities mit Refines headless Ressourcen- und Datenlogik.

## Installation

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## Schnellstart

```tsx
import React from "react";
import { Refine } from "@refinedev/core";
import {
  ErrorComponent,
  ThemedLayoutV2,
  useNotificationProvider,
  RefineThemes,
} from "@refinedev/mantine";
import dataProvider from "@refinedev/simple-rest";
import RouterProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";
import { NotificationsProvider } from "@mantine/notifications";
import { MantineProvider, Global } from "@mantine/core";

export default function App() {
  return (
    <BrowserRouter>
      <MantineProvider
        theme={RefineThemes.Blue}
        withNormalizeCSS
        withGlobalStyles
      >
        <Global styles={{ body: { WebkitFontSmoothing: "auto" } }} />{" "}
        <NotificationsProvider position="top-right">
          <Refine
            routerProvider={RouterProvider}
            dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
            notificationProvider={useNotificationProvider}
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
        </NotificationsProvider>
      </MantineProvider>
    </BrowserRouter>
  );
}
```

Weitere Details findest du in der [Refine documentation](https://refine.dev/docs/) und in den [tutorials](https://refine.dev/docs/tutorial/introduction/index/).
