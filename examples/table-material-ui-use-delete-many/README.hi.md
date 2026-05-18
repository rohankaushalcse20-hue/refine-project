## Material UI useDeleteMany table example

यह example दिखाता है कि **Refine** और Material UI table में multiple records को delete करने का workflow कैसे बनाया जाता है। इसमें row selection और bulk delete action को साथ में दिखाया गया है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example table-material-ui-use-delete-many
```

## मुख्य बिंदु

- selected rows पर `useDeleteMany` action चलाना
- Material UI table selection को bulk operation से जोड़ना
- delete operation के बाद list state को refresh करना
- command, hook names और CodeSandbox URL को original example जैसा रखना

[table-material-ui-use-delete-many example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-material-ui-use-delete-many?view=preview&theme=dark&codemirror=1)
