# Inferencer for refine

`@refinedev/inferencer` आपकी API या resource structure के आधार पर list, show, edit और create views के लिए शुरुआती code generate करता है। इसका लक्ष्य repetitive CRUD page setup कम करना है, ताकि generated code को बाद में customize किया जा सके।

## Installation

```sh
npm install @refinedev/inferencer
```

## Basic usage

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";

const App = () => (
  <Refine>
    <AntdInferencer action="list" resource="posts" />
  </Refine>
);
```

जब आपको नए resource के लिए quick prototype या editable starting point चाहिए, तब Inferencer उपयोगी है।

Details के लिए [Inferencer documentation](https://refine.dev/docs/packages/documentation/inferencer/) और [tutorial section](https://refine.dev/docs/tutorial/getting-started/antd/generate-crud-pages/#inferencer) देखें।
