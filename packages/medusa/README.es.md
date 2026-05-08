# Integración Medusa Store

`@refinedev/medusa` aporta una integración orientada a tiendas y paneles de operación construidos sobre Medusa. Permite conectar tanto la capa de datos como el flujo de autenticación con una configuración inicial sencilla.

## Instalación

```sh
npm install @refinedev/medusa
```

## Uso básico

```tsx
import dataProvider, { authProvider } from "@refinedev/medusa";

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider("API_URL")}
      authProvider={authProvider("API_URL")}
    >
      {/* ... */}
    </Refine>
  );
};
```

## Cuándo usarlo

Úsalo cuando necesites construir herramientas internas, dashboards o paneles administrativos para un backend de comercio basado en Medusa.

## Más información

Consulta la documentación principal de Refine y los materiales de Medusa para ajustar autenticación, resources y operaciones del catálogo.
