## Headless authentication example

यह example **Refine** के headless mode में authentication flow समझाता है। UI framework पर निर्भर हुए बिना `authProvider` login, logout और protected route behavior को संभालता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-headless
```

## मुख्य बिंदु

- custom UI के साथ headless authentication pattern
- `authProvider` से login, logout और identity checks
- route protection को Refine resource structure से जोड़ना
- commands, URLs और hook names को original example जैसा रखना

[auth-headless example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-headless?view=preview&theme=dark&codemirror=1)
