# Integracion de Appwrite para Refine

`@refinedev/appwrite` conecta Refine con proyectos [Appwrite](https://appwrite.io/). Incluye helpers para `dataProvider`, `liveProvider` y autenticacion, de modo que una aplicacion CRUD pueda usar las APIs de Appwrite sin acoplarse a una UI especifica.

## Instalacion

```sh
npm install @refinedev/appwrite
```

## Uso basico

```tsx
import { dataProvider, liveProvider } from "@refinedev/appwrite";

const App = () => (
  <Refine
    dataProvider={dataProvider(appwriteClient, {
      databaseId: "DATABASE_ID",
    })}
    liveProvider={liveProvider(appwriteClient, {
      databaseId: "DATABASE_ID",
    })}
  >
    {/* ... */}
  </Refine>
);
```

## Documentacion

Consulta la [documentacion de Refine](https://refine.dev/docs/) para mas detalles sobre data providers, realtime y autenticacion.
