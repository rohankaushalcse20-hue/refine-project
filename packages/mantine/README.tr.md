# Refine icin Mantine entegrasyonu

`@refinedev/mantine`, Refine'i [Mantine](https://mantine.dev/) ile entegre eder. Mantine temasi, layout'lari, form yardimcilari ve CRUD component'leriyle internal tool ve dashboard arayuzleri kurmaya yardim eder.

## Kurulum

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## Temel kullanim

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

## Dokumantasyon

- [Refine Mantine dokumantasyonunu](https://refine.dev/docs/ui-integrations/mantine/introduction) inceleyin.
- Tam ornek akislari icin [Refine tutorial'lerine](https://refine.dev/docs/tutorial/introduction/index/) bakin.
