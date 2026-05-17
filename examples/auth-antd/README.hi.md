## Ant Design authentication example

यह example **Refine** और Ant Design के साथ authentication flow दिखाता है। इसमें login, protected pages और authenticated resources को `authProvider` से जोड़ा गया है ताकि admin interface access control के साथ चल सके।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-antd
```

## मुख्य बिंदु

- Ant Design UI के साथ `authProvider` integration
- login state के आधार पर protected routes दिखाना
- authenticated CRUD screens और navigation
- commands, URLs और API names को original example जैसा रखना

[auth-antd example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-antd?view=preview&theme=dark&codemirror=1)
