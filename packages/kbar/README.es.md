# Integracion de kbar para Refine

`@refinedev/kbar` agrega una paleta de comandos basada en [kbar](https://github.com/timc1/kbar) a aplicaciones Refine. Es util para ofrecer navegacion rapida entre recursos, acciones y pantallas.

## Instalacion

```sh
npm install @refinedev/kbar
```

## Uso basico

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";

const App = () => (
  <RefineKbarProvider>
    <Refine>{/* ... */}</Refine>
    <RefineKbar />
  </RefineKbarProvider>
);
```

La integracion mantiene sincronizadas las acciones de Refine con la experiencia de busqueda y navegacion de la paleta.

## Documentacion

Consulta el [ejemplo de command palette de Refine](https://refine.dev/docs/examples/command-palette/) para opciones de configuracion y uso.
