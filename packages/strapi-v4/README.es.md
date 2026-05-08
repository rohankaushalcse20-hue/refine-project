# Integración Strapi v4

`@refinedev/strapi-v4` ofrece un data provider y utilidades de autenticación para proyectos que usan Strapi v4 como backend. Facilita la conexión con colecciones, operaciones CRUD y flujos de acceso comunes en paneles administrativos.

## Instalación

```sh
npm install @refinedev/strapi-v4 axios
```

## Uso básico

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

## Cuándo usarlo

Úsalo cuando tu proyecto dependa de Strapi v4 y quieras una integración directa con la capa de datos de Refine sin escribir un provider desde cero.

## Más información

Consulta la documentación de Refine para Strapi v4 y los ejemplos oficiales para adaptar filtros, autenticación y queries personalizadas.
