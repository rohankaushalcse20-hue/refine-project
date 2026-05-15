# refine devtools

`@refinedev/devtools` development mode में refine applications को debug और inspect करने के लिए tools देता है। Devtools queries और mutations monitor करने, inferencer generated code देखने, और refine packages को UI से manage करने जैसे workflows के लिए बनाए गए हैं।

## Installation

पहले latest refine CLI install करें:

```bash
npm install @refinedev/cli@latest
```

फिर devtools setup चलाएं:

```bash
npm run refine devtools init
```

> अगर project में `@refinedev/cli` पहले से नहीं है, तो [CLI installation guide](https://refine.dev/docs/packages/cli/#how-to-add-to-an-existing-project) देखें।

Devtools केवल development mode में चलते हैं और production bundle पर overhead नहीं जोड़ते।
