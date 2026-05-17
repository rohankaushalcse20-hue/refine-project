## Mantine authentication example

यह example दिखाता है कि **Refine** और Mantine UI के साथ login flow और protected resources कैसे configured होते हैं। `authProvider` session checks संभालता है और Mantine components user-facing screens बनाते हैं।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-mantine
```

## मुख्य बिंदु

- Mantine components के साथ authentication screens
- `authProvider` methods से authenticated state संभालना
- protected CRUD pages और application layout
- commands और provider API names को original example जैसा रखना

[auth-mantine example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-mantine?view=preview&theme=dark&codemirror=1)
