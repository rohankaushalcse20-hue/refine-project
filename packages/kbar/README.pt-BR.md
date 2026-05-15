# Integracao kbar para refine

`@refinedev/kbar` adiciona uma paleta de comandos baseada no [kbar](https://kbar.vercel.app/) a aplicacoes refine. Ela permite expor navegacao e acoes frequentes por uma interface command+k.

## Instalacao

```sh
npm install @refinedev/kbar
```

## Uso basico

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";

const App = () => (
  <RefineKbarProvider>
    <Refine>
      <RefineKbar />
    </Refine>
  </RefineKbarProvider>
);
```

Use este pacote quando usuarios avancados precisarem navegar e executar acoes com menos cliques em dashboards e ferramentas internas.

## Documentacao

- Consulte o [exemplo de command palette do refine](https://refine.dev/docs/examples/command-palette/).
- Leia a [documentacao do refine](https://refine.dev/docs/).
