# Inferencer do refine

`@refinedev/inferencer` gera telas iniciais para recursos a partir da estrutura dos dados. O objetivo e acelerar a criacao de paginas CRUD e entregar um ponto de partida que ainda pode ser customizado.

## Instalacao

```sh
npm install @refinedev/inferencer
```

## Uso basico

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";

const App = () => (
  <Refine>
    <AntdInferencer action="list" resource="posts" />
  </Refine>
);
```

Use o Inferencer para explorar rapidamente uma API, validar modelos de dados e gerar telas que depois podem ser refinadas manualmente.

## Documentacao

- Consulte a [documentacao do Inferencer](https://refine.dev/docs/packages/documentation/inferencer/).
- Veja a secao de [Inferencer no tutorial](https://refine.dev/docs/tutorial/getting-started/antd/generate-crud-pages/#inferencer).
