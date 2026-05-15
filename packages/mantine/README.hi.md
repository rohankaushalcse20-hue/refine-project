# Mantine integration for refine

`@refinedev/mantine` refine applications में [Mantine](https://mantine.dev/) components, themes, layout और notification helpers जोड़ता है। यह refine के CRUD, routing और provider workflows को Mantine UI के साथ इस्तेमाल करने के लिए तैयार integration देता है।

## Installation

```sh
npm install @refinedev/mantine @refinedev/react-table @mantine/core@5 @mantine/hooks@5 @mantine/form@5 @mantine/notifications@5 @emotion/react @tabler/icons
```

## Basic usage

```tsx
import { Refine } from "@refinedev/core";
import {
  RefineThemes,
  ThemedLayoutV2,
  useNotificationProvider,
} from "@refinedev/mantine";
import { MantineProvider } from "@mantine/core";

const App = () => (
  <MantineProvider theme={RefineThemes.Blue}>
    <Refine notificationProvider={useNotificationProvider}>
      <ThemedLayoutV2>{/* routes */}</ThemedLayoutV2>
    </Refine>
  </MantineProvider>
);
```

जब project Mantine design system पर बना हो और refine के data hooks, resources और routing behavior चाहिए हों, तब यह package उपयोगी है।

अधिक जानकारी के लिए [Mantine integration documentation](https://refine.dev/docs/ui-integrations/mantine/introduction) देखें।
