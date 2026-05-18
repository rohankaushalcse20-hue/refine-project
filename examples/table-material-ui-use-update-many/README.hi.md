## Material UI useUpdateMany table example

यह example दिखाता है कि **Refine** और Material UI table में multiple records को update करने का workflow कैसे बनाया जाता है। इसमें selected rows पर एक साथ mutation चलाने का pattern शामिल है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example table-material-ui-use-update-many
```

## मुख्य बिंदु

- selected rows के लिए `useUpdateMany` hook का उपयोग
- Material UI table selection से bulk update action चलाना
- mutation result के बाद list view को update करना
- command, hook names और URLs को original example जैसा रखना

[table-material-ui-use-update-many example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-material-ui-use-update-many?view=preview&theme=dark&codemirror=1)
