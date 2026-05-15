# Integracao Material UI para refine

`@refinedev/mui` integra o refine ao [Material UI](https://mui.com/material-ui/getting-started/). Use este pacote para construir ferramentas internas, dashboards e paineis administrativos com componentes Material UI e a logica headless do refine.

## Instalacao

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Inicio rapido

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mui";
import dataProvider from "@refinedev/simple-rest";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";

export default function App() {
  return (
    <BrowserRouter>
      <Refine
        dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
        routerProvider={routerProvider}
        resources={[{ name: "products", list: "/products" }]}
      >
        <Routes>
          <Route element={<ThemedLayoutV2><Outlet /></ThemedLayoutV2>}>
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

## Documentacao

- Consulte a [documentacao Material UI do refine](https://refine.dev/docs/ui-integrations/material-ui/introduction).
- Veja o [tutorial completo do refine](https://refine.dev/tutorial).
