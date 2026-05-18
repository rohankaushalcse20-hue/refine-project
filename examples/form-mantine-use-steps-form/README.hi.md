## Mantine useStepsForm example

यह example दिखाता है कि **Refine** और Mantine के साथ multi-step forms कैसे बनाए जाते हैं। इसमें `useStepsForm` form state को steps में बांटता है और final submit को resource mutation से जोड़ता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example form-mantine-use-steps-form
```

## मुख्य बिंदु

- Mantine UI के साथ step based form flow
- `useStepsForm` से current step और form data संभालना
- लंबे create/edit workflows को छोटे steps में रखना
- command, hook names और CodeSandbox URL को original example जैसा रखना

[form-mantine-use-steps-form example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-mantine-use-steps-form?view=preview&theme=dark&codemirror=1)
