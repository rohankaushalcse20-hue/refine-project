# Integracja Chakra UI dla Refine

`@refinedev/chakra-ui` łączy Refine z [Chakra UI](https://chakra-ui.com/). Pakiet dodaje gotowe komponenty, struktury layoutu, formularze, przyciski i komponenty field dla aplikacji, które potrzebują dostępnego i modułowego interfejsu.

## Instalacja

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Podstawowe użycie

```tsx
import { Refine } from "@refinedev/core";
import { RefineThemes, ThemedLayoutV2 } from "@refinedev/chakra-ui";
import { ChakraProvider } from "@chakra-ui/react";

const App = () => (
  <ChakraProvider theme={RefineThemes.Blue}>
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </ChakraProvider>
);
```

Integracja zostawia logikę biznesową w Refine i dostarcza komponenty Chakra UI dla list, stron tworzenia, edycji i podglądu.

## Dokumentacja

- Przeczytaj [dokumentację Refine Chakra UI](https://refine.dev/docs/ui-integrations/chakra-ui/introduction).
- Pełny scenariusz znajdziesz w [tutorialu Refine](https://refine.dev/tutorial).
