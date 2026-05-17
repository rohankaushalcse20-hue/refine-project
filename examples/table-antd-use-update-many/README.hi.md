## Ant Design useUpdateMany example

यह example **Refine** और Ant Design table में bulk update action बनाना दिखाता है। Selected rows को `useUpdateMany` hook से एक साथ update करके admin workflows तेज किए जाते हैं।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example table-antd-use-update-many
```

## मुख्य बिंदु

- Ant Design row selection के साथ batch update flow
- `useUpdateMany` से multiple records update करना
- mutation result के बाद table state sync रखना
- commands, URLs और hook names को original example जैसा रखना

[table-antd-use-update-many example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-antd-use-update-many?view=preview&theme=dark&codemirror=1)
