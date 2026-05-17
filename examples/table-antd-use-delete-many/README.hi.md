## Ant Design useDeleteMany example

यह example **Refine** और Ant Design table में bulk delete action बनाना दिखाता है। Selected rows को `useDeleteMany` hook से delete करके list page में batch operations जोड़े जाते हैं।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example table-antd-use-delete-many
```

## मुख्य बिंदु

- Ant Design row selection के साथ bulk actions
- `useDeleteMany` से multiple records delete करना
- delete mutation के बाद table data refresh करना
- commands, URLs और hook names को original example जैसा रखना

[table-antd-use-delete-many example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-antd-use-delete-many?view=preview&theme=dark&codemirror=1)
