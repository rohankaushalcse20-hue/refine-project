# Ant Design integration for refine

`@refinedev/antd` refine applications में [Ant Design](https://ant.design/) components, layout, forms, tables और notification helpers जोड़ता है। यह package refine के headless CRUD foundation को Ant Design के ready-made UI primitives से जोड़कर admin panels, dashboards और internal tools तेजी से बनाने में मदद करता है।

## Installation

```sh
npm install @refinedev/antd antd
```

## Basic usage

```tsx
import { Refine } from "@refinedev/core";
import { ThemedLayoutV2 } from "@refinedev/antd";

const App = () => (
  <Refine>
    <ThemedLayoutV2>{/* routes */}</ThemedLayoutV2>
  </Refine>
);
```

जब आप Ant Design के tables, forms और layout conventions के साथ refine resources को render करना चाहते हैं, तब यह integration अच्छा default है।

अधिक जानकारी के लिए [Ant Design integration documentation](https://refine.dev/docs/ui-integrations/ant-design/introduction) और [refine tutorial](https://refine.dev/tutorial) देखें।
