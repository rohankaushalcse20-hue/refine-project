## useImport example

यह example **Refine** के `useImport` hook से bulk import workflow बनाना दिखाता है। CSV जैसे inputs को resource records में बदलकर data provider के माध्यम से create operations चलाए जा सकते हैं।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example core-use-import
```

## मुख्य बिंदु

- `useImport` hook के साथ file import flow
- imported rows को Refine resources से map करना
- bulk create operations और error handling का pattern
- commands, hook names और API names को original example जैसा रखना

[core-use-import example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/core-use-import?view=preview&theme=dark&codemirror=1)
