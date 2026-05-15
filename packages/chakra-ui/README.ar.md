# تكامل Chakra UI مع Refine

تدمج حزمة `@refinedev/chakra-ui` بين Refine و[Chakra UI](https://chakra-ui.com/). وهي توفر layouts وأزراراً وحقولاً وhooks مهيأة لتدفقات CRUD، مع إبقاء منطق البيانات وrouting وauthentication والصلاحيات منفصلاً.

## التثبيت

```sh
npm install @refinedev/chakra-ui @chakra-ui/react @emotion/react @emotion/styled framer-motion
```

## الاستخدام الأساسي

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

الحزمة مناسبة عندما تريد واجهة قابلة للوصول والتركيب باستخدام Chakra UI من دون إعادة تنفيذ أنماط الإدارة الشائعة.

## التوثيق

- راجع [توثيق Refine مع Chakra UI](https://refine.dev/docs/ui-integrations/chakra-ui/introduction).
- راجع [دروس Refine](https://refine.dev/docs/tutorial/introduction/index/) لرؤية تدفقات كاملة.
