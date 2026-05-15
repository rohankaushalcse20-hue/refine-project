# Integracao Airtable para refine

`@refinedev/airtable` e um data provider para usar bases do [Airtable](https://www.airtable.com/) em aplicacoes refine. Ele permite criar telas CRUD sobre tabelas relacionais hospedadas no Airtable sem acoplar a aplicacao a uma biblioteca de UI especifica.

## Instalacao

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

Use este pacote quando o Airtable for a fonte de dados principal para prototipos, operacoes internas ou paineis administrativos.

## Documentacao

- Leia a [documentacao de data provider do refine](https://refine.dev/docs/core/providers/data-provider).
- Consulte o [exemplo Airtable do refine](https://refine.dev/docs/examples/data-provider/airtable/).
