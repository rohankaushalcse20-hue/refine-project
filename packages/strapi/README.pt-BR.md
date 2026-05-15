# Data provider Strapi para refine

`@refinedev/strapi` oferece uma integracao para backends Strapi. Com ele, voce pode gerenciar conteudos do Strapi em listas, paginas de detalhes, criacao e edicao do Refine.

## Instalacao

```sh
npm install @refinedev/strapi axios
```

## Uso basico

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi";

const axiosInstance = axios.create();
const strapiAuthHelper = AuthHelper("API_URL");

const App = () => {
  return (
    <Refine
      dataProvider={DataProvider("API_URL", axiosInstance)}
      /* ... */
    >
      {/* ... */}
    </Refine>
  );
};
```

## Documentacao

- Consulte a [documentacao de data providers do refine](https://refine.dev/docs/core/providers/data-provider).
- Veja o [exemplo de data provider Strapi](https://refine.dev/docs/examples/data-provider/strapi/).
