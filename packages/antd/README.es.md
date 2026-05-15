# Integracion de Ant Design para Refine

`@refinedev/antd` integra Refine con [Ant Design](https://ant.design/). Incluye componentes, hooks y layouts preparados para construir paneles administrativos, dashboards y aplicaciones B2B con una experiencia visual consistente.

## Instalacion

```sh
npm install @refinedev/antd antd
```

## Uso basico

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/antd";

import "antd/dist/reset.css";

const App = () => (
  <Refine>
    <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
  </Refine>
);
```

El paquete mantiene la logica headless de Refine y aporta primitivas de Ant Design como `List`, `Create`, `Edit`, `Show`, `useTable` y campos de presentacion.

## Documentacion

- Consulta la [documentacion de Refine con Ant Design](https://refine.dev/docs/ui-integrations/ant-design/introduction).
- Revisa el [tutorial completo de Refine](https://refine.dev/tutorial).
