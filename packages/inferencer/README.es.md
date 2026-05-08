# Inferencer de Refine

`@refinedev/inferencer` genera vistas CRUD a partir de la estructura de tus datos para que puedas arrancar más rápido y luego ajustar el resultado manualmente. Es especialmente útil cuando estás explorando una API o construyendo un panel administrativo inicial.

## Instalación

```sh
npm install @refinedev/inferencer
```

## Uso básico

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";

const App = () => {
  return (
    <Refine>
      <AntdInferencer action="list" resource="posts" />
    </Refine>
  );
};
```

## Cuándo usarlo

Usa Inferencer cuando necesites prototipar pantallas rápidamente, inspeccionar la forma de una API o generar una primera versión editable de tus vistas CRUD.

## Más información

Revisa la documentación de Inferencer y el tutorial de Refine para adaptar las vistas generadas a tu proyecto.
