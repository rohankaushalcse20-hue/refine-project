# Chakra UI integration for refine

`@refinedev/chakra-ui` refine applications के लिए [Chakra UI](https://chakra-ui.com/) आधारित UI helpers देता है। इसमें layout, themed components, notification provider और refine workflows के साथ काम करने वाले building blocks शामिल हैं।

## Installation

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## Basic usage

```tsx
import { Refine } from "@refinedev/core";
import {
  RefineThemes,
  ThemedLayoutV2,
  useNotificationProvider,
} from "@refinedev/chakra-ui";
import { ChakraProvider } from "@chakra-ui/react";

const App = () => (
  <ChakraProvider theme={RefineThemes.Blue}>
    <Refine notificationProvider={useNotificationProvider()}>
      <ThemedLayoutV2>{/* routes */}</ThemedLayoutV2>
    </Refine>
  </ChakraProvider>
);
```

यह package तब उपयोगी है जब आपको accessible Chakra UI components के साथ refine की data, auth, routing और notification capabilities चाहिए।

अधिक जानकारी के लिए [Chakra UI integration documentation](https://refine.dev/docs/ui-integrations/chakra-ui/introduction) देखें।
