# Integracion de Strapi para Refine

`@refinedev/strapi` conecta Refine con APIs de [Strapi](https://strapi.io/). Incluye helpers para data provider y autenticacion, de modo que puedas construir paneles administrativos sobre contenido gestionado en Strapi.

## Instalacion

```sh
npm install @refinedev/strapi axios
```

## Uso basico

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi";
import axios from "axios";

const axiosInstance = axios.create();
const authHelper = AuthHelper("API_URL");

const App = () => (
  <Refine dataProvider={DataProvider("API_URL", axiosInstance)}>
    {/* ... */}
  </Refine>
);
```

## Documentacion

Consulta la [documentacion de Refine](https://refine.dev/docs/) para combinar Strapi con autenticacion, recursos y formularios.
