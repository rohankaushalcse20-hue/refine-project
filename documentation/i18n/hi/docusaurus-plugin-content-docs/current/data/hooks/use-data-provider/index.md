---
title: "useDataProvider Hook | Refine v5"
display_title: "useDataProvider"
sidebar_label: "useDataProvider"
description: "Refine v5 में multiple data providers के साथ useDataProvider hook का Hindi परिचय।"
source: packages/core/src/data/hooks/useDataProvider.tsx
---

`useDataProvider` एक React hook है जो [`<Refine>`][Refine] component को दिए गए `dataProvider` तक पहुंच लौटाता है।

यह खास तौर पर तब उपयोगी होता है जब आपके पास कई data providers हों और आपको उनमें से किसी एक को programmatically access करना हो।

## Usage

मान लें कि हमारे पास दो data providers हैं:

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine
    dataProvider={{
      default: dataProvider("API_URL"),
      second: dataProvider("SECOND_API_URL"),
    }}
  >
    {/* ... */}
  </Refine>
);
```

अब `useDataProvider` hook की मदद से हम इन providers तक पहुंच सकते हैं:

```tsx
import { useDataProvider } from "@refinedev/core";

const dataProvider = useDataProvider();

const defaultDataProvider = dataProvider(); // default data provider लौटाता है
const secondDataProvider = dataProvider("second"); // second data provider लौटाता है
```

## API Reference

### Properties

| Property         | Description                                      | Type     | Default   |
| ---------------- | ------------------------------------------------ | -------- | --------- |
| dataProviderName | जिस data provider को access करना है उसका नाम     | `string` | `default` |

### Return value

| Description   | Type                                              |
| ------------- | ------------------------------------------------- |
| Data Provider | [`Data Provider`](/core/docs/data/data-provider/) |

[Refine]: /core/docs/core/refine-component
[data provider]: /core/docs/data/data-provider
