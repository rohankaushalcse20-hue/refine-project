## Ant Design useStepsForm example

यह example **Refine** और Ant Design में multi-step forms बनाना दिखाता है। `useStepsForm` hook लंबे create/edit workflows को छोटे steps में बांटकर validation और submit flow संभालता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example form-antd-use-steps-form
```

## मुख्य बिंदु

- Ant Design `Steps` component के साथ step-based form
- हर step के लिए form state और validation control
- अंतिम submit पर Refine mutation चलाना
- commands, URLs और hook names को original example जैसा रखना

[form-antd-use-steps-form example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-antd-use-steps-form?view=preview&theme=dark&codemirror=1)
