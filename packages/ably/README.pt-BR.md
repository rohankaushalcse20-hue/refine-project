# Integracao Ably para refine

`@refinedev/ably` fornece um `liveProvider` baseado no [Ably](https://ably.com/) para aplicacoes refine. Use este pacote quando sua ferramenta interna, dashboard ou painel administrativo precisar receber atualizacoes em tempo real por WebSocket.

## Instalacao

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

O provider conecta os eventos do Ably ao contrato de realtime do refine, mantendo a logica de dados separada da camada visual.

## Documentacao

- Consulte a [documentacao de live provider do refine](https://refine.dev/docs/api-references/providers/live-provider/).
- Veja tambem o [tutorial oficial da Ably com refine](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine).
