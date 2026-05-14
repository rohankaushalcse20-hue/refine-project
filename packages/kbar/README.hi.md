# Command palette integration with kbar for refine

`@refinedev/kbar` Refine applications में command palette जोड़ने के लिए kbar integration देता है। इससे users keyboard-driven navigation और actions के जरिए resources तक जल्दी पहुंच सकते हैं।

## Installation

```sh
npm install @refinedev/kbar
```

## Basic usage

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";

const App = () => (
  <RefineKbarProvider>
    <Refine>
      <RefineKbar />
    </Refine>
  </RefineKbarProvider>
);
```

Admin panels और dense internal tools में frequently used actions को command palette से expose करने के लिए यह package उपयोगी है।

अधिक जानकारी के लिए [Refine kbar example](https://refine.dev/docs/examples/command-palette/) और [documentation](https://refine.dev/docs/) देखें।
