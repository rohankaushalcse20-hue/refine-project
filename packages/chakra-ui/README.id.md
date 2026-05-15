# Integrasi Chakra UI untuk Refine

Package `@refinedev/chakra-ui` menghubungkan Refine dengan [Chakra UI](https://chakra-ui.com/). Package ini menyediakan layouts, tombol, field, dan hooks yang disiapkan untuk workflow CRUD, sambil menjaga data, routing, authentication, dan authorization tetap terpisah.

## Instalasi

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Penggunaan dasar

```tsx
import { Refine } from "@refinedev/core";
import { ChakraProvider } from "@chakra-ui/react";
import { RefineThemes, ThemedLayoutV2 } from "@refinedev/chakra-ui";

const App = () => (
  <ChakraProvider theme={RefineThemes.Blue}>
    <Refine>
      <ThemedLayoutV2>{/* ... */}</ThemedLayoutV2>
    </Refine>
  </ChakraProvider>
);
```

Package ini cocok saat Anda membutuhkan UI yang accessible dan composable dengan Chakra UI tanpa membangun ulang pola admin yang umum.

## Dokumentasi

- Baca [dokumentasi Refine dengan Chakra UI](https://refine.dev/docs/ui-integrations/chakra-ui/introduction).
- Baca [tutorial Refine](https://refine.dev/docs/tutorial/introduction/index/) untuk melihat workflow lengkap.
