# Simple REST Data Provider

`@refinedev/simple-rest` oferece um data provider para REST APIs com uma estrutura padronizada. Ele segue um estilo semelhante ao `json-server` e conecta resources do Refine a endpoints HTTP.

## Instalação

```sh
npm install @refinedev/simple-rest
```

## Uso básico

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

## Quando usar

Use este provider quando seu backend expuser endpoints REST simples para listar, criar, atualizar e excluir registros. Se a API precisar de autenticação, headers customizados ou parâmetros especiais, você pode estender ou encapsular o provider.

## Mais informações

A documentação do Refine sobre data providers mostra como adaptar a integração ao seu backend.
