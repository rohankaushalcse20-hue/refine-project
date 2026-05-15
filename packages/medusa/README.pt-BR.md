# Integracao Medusa para refine

`@refinedev/medusa` conecta aplicacoes refine a backends [Medusa](https://medusajs.com/) para experiencias de comercio. O pacote fornece data provider e auth provider para montar paineis administrativos e ferramentas operacionais.

## Instalacao

```sh
npm install @refinedev/medusa
```

## Uso basico

```tsx
import dataProvider, { authProvider } from "@refinedev/medusa";

const App = () => (
  <Refine
    dataProvider={dataProvider("API_URL")}
    authProvider={authProvider("API_URL")}
  >
    {/* ... */}
  </Refine>
);
```

## Documentacao

- Consulte a [documentacao de data provider do refine](https://refine.dev/docs/core/providers/data-provider).
- Veja os [tutoriais do refine](https://refine.dev/docs/tutorial/introduction/index/).
