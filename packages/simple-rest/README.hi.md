# Simple REST data provider

`@refinedev/simple-rest` standard shape वाली REST APIs के लिए data provider देता है। यह `json-server` शैली के endpoints के साथ अच्छी तरह काम करता है और Refine resources को HTTP operations से जोड़ता है।

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

जब आपका backend list, create, update और delete के लिए सरल REST endpoints expose करता हो, तब यह provider अच्छा शुरुआती विकल्प है। जरूरत पड़ने पर आप इसे custom headers, params या auth logic के साथ wrap भी कर सकते हैं।
