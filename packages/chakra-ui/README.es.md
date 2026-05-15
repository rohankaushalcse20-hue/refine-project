# Integracion de Chakra UI para Refine

`@refinedev/chakra-ui` integra Refine con [Chakra UI](https://chakra-ui.com/). Proporciona layouts, botones, campos y hooks adaptados a flujos CRUD manteniendo separada la logica de datos, routing, autenticacion y permisos.

## Instalacion

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Uso basico

```tsx
import { Refine } from "@refinedev/core";
import { ChakraProvider } from "@chakra-ui/react";
import { RefineThemes, ThemedLayoutV2 } from "@refinedev/chakra-ui";

const App = () => (
  <ChakraProvider theme={RefineThemes.Blue}>
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </ChakraProvider>
);
```

El paquete es adecuado cuando quieres una interfaz accesible y componible con Chakra UI sin reimplementar patrones comunes de administracion.

## Documentacion

- Consulta la [documentacion de Refine con Chakra UI](https://refine.dev/docs/ui-integrations/chakra-ui/introduction).
- Revisa los [tutoriales de Refine](https://refine.dev/docs/tutorial/introduction/index/) para ver flujos completos.
