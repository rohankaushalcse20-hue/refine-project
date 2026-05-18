## Mantine useForm example

यह example दिखाता है कि **Refine** और Mantine के साथ create/edit forms कैसे बनाए जाते हैं। इसमें `useForm` hook form state, validation और submit flow को resource mutation से जोड़ता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example form-mantine-use-form
```

## मुख्य बिंदु

- Mantine form components के साथ `useForm` integration
- create और edit pages के लिए shared form workflow
- submit action को Refine mutation lifecycle से जोड़ना
- command, hook names और URLs को original example जैसा रखना

[form-mantine-use-form example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-mantine-use-form?view=preview&theme=dark&codemirror=1)
