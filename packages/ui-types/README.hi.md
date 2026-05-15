# refine UI types

`@refinedev/ui-types` refine UI integrations के बीच shared TypeScript types उपलब्ध कराता है। यह package reusable component props, layout contracts और UI provider boundaries को consistent रखने में मदद करता है।

## Installation

```sh
npm install @refinedev/ui-types
```

## कब उपयोग करें

- refine-compatible UI package बनाते समय shared props reuse करने के लिए
- internal design-system wrappers में refine UI contracts type करने के लिए
- package boundaries पर component APIs को consistent रखने के लिए

Application code में इसे अक्सर सीधे import करने की जरूरत नहीं होती; यह मुख्य रूप से refine UI packages और advanced integrations के लिए support package है।
