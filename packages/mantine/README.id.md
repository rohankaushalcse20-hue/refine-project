# Integrasi Mantine untuk Refine

Package `@refinedev/mantine` menghubungkan Refine dengan [Mantine](https://mantine.dev/). Package ini menambahkan layouts, komponen, dan themes siap pakai untuk membangun internal tools dan dashboards dengan UI Mantine yang konsisten.

## Instalasi

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## Penggunaan dasar

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

## Dokumentasi

- Baca [dokumentasi Refine dengan Mantine](https://refine.dev/docs/ui-integrations/mantine/introduction).
- Baca [tutorial Refine](https://refine.dev/docs/tutorial/introduction/index/) untuk contoh lengkap.
