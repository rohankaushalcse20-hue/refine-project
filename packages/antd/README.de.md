# Ant Design integration for Refine

`@refinedev/antd` stellt Refine-Komponenten und Hooks fuer [Ant Design](https://ant.design/) bereit. Damit kannst du Refines headless Daten-, Routing- und Formularlogik mit Ant Design Layouts, Tabellen, Formularen und Feedback-Komponenten kombinieren.

## Installation

```sh
npm install @refinedev/antd antd
```

## Schnellstart

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/antd";
import dataProvider from "@refinedev/simple-rest";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";

import "antd/dist/reset.css";

export default function App() {
  return (
    <BrowserRouter>
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

Nutze dieses package, wenn du Ant Design als UI-Schicht fuer Refine-Adminpanels, Dashboards oder interne Tools einsetzen moechtest.

Weitere Details findest du in der [Refine documentation](https://refine.dev/docs/) und in den [tutorials](https://refine.dev/docs/tutorial/introduction/index/).
