---
title: Data Fetching
---

import { Sandpack, FocusOnDataProviderFile, AddDataProviderToRefine } from "./sandpack.tsx";

<Sandpack>

En este paso aprenderemos los fundamentos de data fetching en Refine. El componente `<Refine />` acepta una prop [`dataProvider`](/core/docs/core/refine-component/#dataprovider-) que se usa para gestionar todas las operaciones de data fetching y mutación mediante una interfaz sencilla. Aunque Refine incluye muchos data providers listos para usar, para este tutorial crearemos nuestro propio data provider y lo conectaremos a una [fake REST API](https://api.fake-rest.refine.dev/).

Para obtener más información sobre los data providers soportados, consulta la sección [Supported Data Providers](/core/docs/guides-concepts/data-fetching/#supported-data-providers) de la guía Data Fetching.

## Crear un Data Provider

Implementaremos cada método uno por uno, asegurándonos de cubrir bien todos los detalles. Usaremos `fetch` para las solicitudes API, pero puedes elegir cualquier librería.

Primero crearemos un archivo `src/providers/data-provider.ts` en nuestro proyecto. Este archivo contendrá todos los métodos que debemos implementar para nuestro data provider.

Para ver un data provider vacío, <FocusOnDataProviderFile>revisa `src/providers/data-provider.ts`</FocusOnDataProviderFile> en el panel derecho.

Después pasaremos nuestro data provider al componente `<Refine />` en el archivo `src/App.tsx` mediante la prop `dataProvider`.

Actualiza tu archivo `src/App.tsx` agregando las siguientes líneas:

```tsx
import { Refine, WelcomePage } from "@refinedev/core";

// highlight-next-line
import { dataProvider } from "./providers/data-provider";

export default function App(): JSX.Element {
  return (
    // highlight-next-line
    <Refine dataProvider={dataProvider}>
      <WelcomePage />
    </Refine>
  );
}
```

<AddDataProviderToRefine />

:::tip

También es posible usar múltiples data providers con Refine. Puedes aprender más en la sección [Multiple Data Providers](/core/docs/guides-concepts/data-fetching/#multiple-data-providers) de la guía Data Fetching.

:::

En el siguiente paso aprenderemos a obtener un registro con el hook `useOne` de Refine y también a implementar el método `getOne` en nuestro data provider.

</Sandpack>
