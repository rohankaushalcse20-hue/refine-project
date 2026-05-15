# Data provider NestJSX CRUD para refine

`@refinedev/nestjsx-crud` integra o Refine a APIs RESTful criadas com NestJSX CRUD. Ele conecta resources do Refine a endpoints que seguem o padrao do NestJSX CRUD.

## Instalacao

```sh
npm install @refinedev/nestjsx-crud
```

## Uso basico

```tsx
import dataProvider from "@refinedev/nestjsx-crud";

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider("API_URL")}
      /* ... */
    >
      {/* ... */}
    </Refine>
  );
};
```

## Quando usar

Use este provider quando seu backend NestJS expuser endpoints compativeis com NestJSX CRUD. Nomes de resources, paths, filtros, sorts e parametros continuam sendo contratos tecnicos da API.

## Documentacao

- Consulte a [documentacao de data providers do refine](https://refine.dev/docs/core/providers/data-provider).
- Veja o [exemplo NestJS CRUD com refine](https://refine.dev/docs/examples/data-provider/nestjsxCrud/).
