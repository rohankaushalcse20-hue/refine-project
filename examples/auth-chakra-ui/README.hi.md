## Chakra UI authentication example

यह example दिखाता है कि **Refine** application में Chakra UI components के साथ authentication screens कैसे बनाए जाते हैं। `authProvider` login state संभालता है और protected resources केवल authenticated users को दिखते हैं।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-chakra-ui
```

## मुख्य बिंदु

- Chakra UI layout के साथ login और protected pages
- `authProvider` methods से session state संभालना
- resources और navigation को authentication status से जोड़ना
- commands और component names को original example जैसा रखना

[auth-chakra-ui example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-chakra-ui?view=preview&theme=dark&codemirror=1)
