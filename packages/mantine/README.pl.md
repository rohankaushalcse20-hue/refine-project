# Integracja Mantine dla Refine

`@refinedev/mantine` integruje Refine z [Mantine](https://mantine.dev/). Pakiet dodaje gotowe komponenty layoutu, przyciski, formularze, powiadomienia, tabele i komponenty field dla aplikacji opartych na Mantine.

## Instalacja

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## Podstawowe użycie

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/mantine";
import { MantineProvider } from "@mantine/core";

const App = () => (
  <MantineProvider>
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </MantineProvider>
);
```

Integracja zachowuje headlessową architekturę Refine i dostarcza implementacje Mantine dla typowych ekranów CRUD.

## Dokumentacja

- Przeczytaj [dokumentację Refine Mantine](https://refine.dev/docs/ui-integrations/mantine/introduction).
- Pełny scenariusz znajdziesz w [tutorialu Refine](https://refine.dev/tutorial).
