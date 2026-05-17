## RTL customization example

यह example दिखाता है कि **Refine** application में right-to-left layout support कैसे enabled किया जा सकता है। यह उन locales के लिए उपयोगी है जहां UI direction `rtl` होती है और layout mirroring जरूरी होती है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example customization-rtl
```

## मुख्य बिंदु

- RTL direction के साथ Refine layout configure करना
- theme और component styles को mirrored UI के लिए तैयार करना
- localized applications में direction-aware navigation
- commands, URLs और configuration names को original example जैसा रखना

[customization-rtl example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/customization-rtl?view=preview&theme=dark&codemirror=1)
