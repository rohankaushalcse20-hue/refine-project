# Data provider NestJSX CRUD para Refine

`@refinedev/nestjsx-crud` integra Refine con APIs REST construidas con [NestJSX CRUD](https://github.com/nestjsx/crud). Permite conectar tus resources de Refine a endpoints NestJSX CRUD sin escribir manualmente las operaciones comunes de listado, creacion, edicion y eliminacion.

## Sobre el paquete

Refine es headless por diseno y ofrece integraciones listas para UI, routing, autenticacion, autorizacion, networking, estado e i18n. Este data provider traduce las operaciones de Refine al formato esperado por NestJSX CRUD para que puedas trabajar con datos desde el frontend de forma consistente.

## Instalacion y uso

```sh
npm install @refinedev/nestjsx-crud
```

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

## Documentacion

- Consulta la [documentacion del data provider de Refine](https://refine.dev/docs/core/providers/data-provider).
- Revisa el [ejemplo de Refine con NestJS CRUD](https://refine.dev/docs/examples/data-provider/nestjsxCrud/).
- Empieza tambien por la [documentacion de Refine](https://refine.dev/docs/) y los [tutoriales](https://refine.dev/docs/tutorial/introduction/index/).
