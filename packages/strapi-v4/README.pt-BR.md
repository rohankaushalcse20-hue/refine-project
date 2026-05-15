# Data provider Strapi v4 para refine

`@refinedev/strapi-v4` oferece uma integracao para backends Strapi v4. Ele conecta resources do Refine a collections do Strapi para listar, criar, editar e visualizar registros.

## Instalacao

```sh
npm install @refinedev/strapi-v4 axios
```

## Uso basico

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi-v4";

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
- Veja a [documentacao do Strapi v4 provider](https://refine.dev/docs/packages/documentation/data-providers/strapi-v4/).
- Veja o [exemplo de data provider Strapi v4](https://refine.dev/docs/examples/data-provider/strapi-v4/).
