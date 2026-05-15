# Integracion de Mantine para Refine

`@refinedev/mantine` integra Refine con [Mantine](https://mantine.dev/). Aporta layouts, componentes y temas preparados para construir herramientas internas y dashboards con una UI Mantine consistente.

## Instalacion

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## Uso basico

```tsx
import { Refine } from "@refinedev/core";
import { MantineProvider } from "@mantine/core";
import { NotificationsProvider } from "@mantine/notifications";
import { RefineThemes, ThemedLayoutV2 } from "@refinedev/mantine";

const App = () => (
  <MantineProvider theme={RefineThemes.Blue} withNormalizeCSS withGlobalStyles>
    <NotificationsProvider position="top-right">
      <Refine>
        <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
      </Refine>
    </NotificationsProvider>
  </MantineProvider>
);
```

## Documentacion

- Consulta la [documentacion de Refine con Mantine](https://refine.dev/docs/ui-integrations/mantine/introduction).
- Revisa los [tutoriales de Refine](https://refine.dev/docs/tutorial/introduction/index/) para ejemplos completos.
