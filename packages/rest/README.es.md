# Data provider REST para Refine

`@refinedev/rest` proporciona un data provider REST generico para aplicaciones Refine. Es util cuando tu backend expone endpoints HTTP y quieres adaptar las operaciones CRUD de Refine a esa API.

## Instalacion

```sh
npm install @refinedev/rest
```

## Uso basico

```tsx
import dataProvider from "@refinedev/rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

## Documentacion

Consulta la [documentacion de data providers de Refine](https://refine.dev/docs/data/data-provider/) para entender el contrato que debe cumplir una API REST.
