# تكامل Mantine مع Refine

تدمج حزمة `@refinedev/mantine` بين Refine و[Mantine](https://mantine.dev/). تضيف layouts ومكونات وthemes جاهزة لبناء أدوات داخلية وdashboards بواجهة Mantine متسقة.

## التثبيت

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## الاستخدام الأساسي

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

## التوثيق

- راجع [توثيق Refine مع Mantine](https://refine.dev/docs/ui-integrations/mantine/introduction).
- راجع [دروس Refine](https://refine.dev/docs/tutorial/introduction/index/) لأمثلة كاملة.
