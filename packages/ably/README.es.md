# Integracion de Ably para Refine

`@refinedev/ably` proporciona un `liveProvider` basado en [Ably](https://ably.com/) para aplicaciones Refine. Usa este paquete cuando una herramienta interna, dashboard o panel administrativo necesita recibir actualizaciones en tiempo real por WebSocket.

## Instalacion

```sh
npm install @refinedev/ably
```

## Uso basico

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => (
  <Refine liveProvider={liveProvider(ablyClient)}>
    {/* ... */}
  </Refine>
);
```

El provider conecta los eventos de Ably con el contrato realtime de Refine y mantiene la logica de datos separada de la capa visual.

## Documentacion

- Consulta la [documentacion del live provider de Refine](https://refine.dev/docs/api-references/providers/live-provider/).
- Revisa tambien el [tutorial oficial de Ably con Refine](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine).
