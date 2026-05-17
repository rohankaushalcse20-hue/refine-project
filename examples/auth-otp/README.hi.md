## OTP authentication example

यह example बताता है कि **Refine** में one-time password login flow कैसे बनाया जा सकता है। `authProvider` OTP request और verification steps को संभालता है, जबकि application authenticated resources को सुरक्षित रखती है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-otp
```

## मुख्य बिंदु

- OTP based login और verification workflow
- `authProvider` के साथ temporary authentication state
- protected resources को verified users तक सीमित रखना
- commands, URLs और API names को original example जैसा रखना

[auth-otp example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-otp?view=preview&theme=dark&codemirror=1)
