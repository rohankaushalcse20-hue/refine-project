# Integracao Ant Design para refine

`@refinedev/antd` combina a logica headless do refine com componentes, layouts, formularios, tabelas e feedback visual do [Ant Design](https://ant.design/).

## Instalacao

```sh
npm install @refinedev/antd antd
```

## Inicio rapido

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

Use esta integracao quando quiser entregar uma interface Ant Design mantendo os providers de dados, roteamento, autenticacao e autorizacao do refine.

## Documentacao

- Consulte a [documentacao Ant Design do refine](https://refine.dev/docs/ui-integrations/ant-design/introduction).
- Veja o [tutorial completo do refine](https://refine.dev/tutorial).
