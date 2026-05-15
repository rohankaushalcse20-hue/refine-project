# Integracao Mantine para refine

`@refinedev/mantine` fornece componentes e hooks para construir interfaces refine com [Mantine](https://mantine.dev/). Ele integra layouts, formularios, notificacoes e tabelas ao fluxo headless do refine.

## Instalacao

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## Inicio rapido

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mantine";
import dataProvider from "@refinedev/simple-rest";
import RouterProvider from "@refinedev/react-router";
import { BrowserRouter, Outlet, Route, Routes } from "react-router";

export default function App() {
  return (
    <BrowserRouter>
      <Refine
        routerProvider={RouterProvider}
        dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
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

- Consulte a [documentacao Mantine do refine](https://refine.dev/docs/ui-integrations/mantine/introduction).
- Veja os [tutoriais do refine](https://refine.dev/docs/tutorial/introduction/index/).
