# Refine icin Chakra UI entegrasyonu

`@refinedev/chakra-ui`, Refine'i [Chakra UI](https://chakra-ui.com/) ile kullanmak icin hazir component'ler, field'lar, layout'lar ve form yardimcilari saglar. Accessible ve temalandirilabilir arayuzler kurmak isteyen ekipler icin uygundur.

## Kurulum

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Temel kullanim

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/chakra-ui";
import { ChakraProvider } from "@chakra-ui/react";

const App = () => (
  <ChakraProvider>
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </ChakraProvider>
);
```

Refine, routing, data provider ve authorization mantigini saglar; Chakra UI ise gorunum ve etkilesim katmanini olusturur.

## Dokumantasyon

- [Refine Chakra UI dokumantasyonunu](https://refine.dev/docs/ui-integrations/chakra-ui/introduction) inceleyin.
- Tam uygulama akislari icin [Refine tutorial'lerine](https://refine.dev/docs/tutorial/introduction/index/) bakin.
