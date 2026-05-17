## Multiple data providers example

यह example **Refine** में एक ही application के अंदर multiple data providers इस्तेमाल करना दिखाता है। अलग-अलग resources को अलग backend providers से जोड़कर complex admin अनुभव तैयार किया जा सकता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example data-provider-multiple
```

## मुख्य बिंदु

- multiple data providers को resource-level configuration से चलाना
- अलग resources के लिए अलग API sources चुनना
- list/create/edit flows को provider names के साथ route करना
- commands, URLs और provider names को original example जैसा रखना

[data-provider-multiple example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-multiple?view=preview&theme=dark&codemirror=1)
