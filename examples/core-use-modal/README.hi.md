## useModal example

यह example **Refine** के `useModal` hook से modal state manage करना दिखाता है। Hook open, close और visibility state देता है ताकि create या edit जैसे workflows को modal UI में रखा जा सके।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example core-use-modal
```

## मुख्य बिंदु

- `useModal` hook से modal visibility संभालना
- CRUD actions को modal-driven UI से जोड़ना
- custom components में open और close handlers reuse करना
- commands, hook names और API names को original example जैसा रखना

[core-use-modal example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/core-use-modal?view=preview&theme=dark&codemirror=1)
