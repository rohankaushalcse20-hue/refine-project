# Integracion de Airtable para Refine

`@refinedev/airtable` ofrece un data provider para conectar aplicaciones Refine con bases de [Airtable](https://www.airtable.com/). Es util para crear paneles internos y herramientas CRUD sobre datos que ya viven en Airtable.

## Instalacion

```sh
npm install @refinedev/airtable
```

## Uso basico

```tsx
import dataProvider from "@refinedev/airtable";

const App = () => (
  <Refine dataProvider={dataProvider("API_KEY", "BASE_ID")}>
    {/* ... */}
  </Refine>
);
```

El provider traduce las operaciones de recursos de Refine a llamadas contra la API de Airtable, sin imponer una libreria de UI concreta.

## Documentacion

- Consulta la [documentacion de data providers de Refine](https://refine.dev/docs/data/data-provider/).
- Revisa la [documentacion principal de Refine](https://refine.dev/docs/) para guias y tutoriales.
