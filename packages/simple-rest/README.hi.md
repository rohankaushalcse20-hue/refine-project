# Simple REST data provider

`@refinedev/simple-rest` उन REST APIs के लिए data provider देता है जिनकी structure standard होती है। यह `json-server` शैली का पालन करता है और Refine resources को HTTP endpoints से जोड़ता है।

## Installation

```sh
npm install @refinedev/simple-rest
```

## Basic usage

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

इस provider का उपयोग तब करें जब backend list, create, update और delete के लिए सरल REST endpoints expose करता हो। Custom headers या special params के लिए आप इसे wrap या extend कर सकते हैं।
