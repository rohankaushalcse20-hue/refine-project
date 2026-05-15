# Integracao Chakra UI para refine

`@refinedev/chakra-ui` fornece componentes e hooks para usar o [Chakra UI](https://chakra-ui.com/) como camada visual de aplicacoes refine.

## Instalacao

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Inicio rapido

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/chakra-ui";
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

Use esta integracao quando quiser construir paineis refine com componentes acessiveis, modulares e tematizaveis do Chakra UI.

## Documentacao

- Consulte a [documentacao Chakra UI do refine](https://refine.dev/docs/ui-integrations/chakra-ui/introduction).
- Veja os [tutoriais do refine](https://refine.dev/docs/tutorial/introduction/index/).
