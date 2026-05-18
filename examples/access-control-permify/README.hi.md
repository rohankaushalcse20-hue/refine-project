## Permify access control example

यह example दिखाता है कि **Refine** application में Permify आधारित authorization कैसे जोड़ी जा सकती है। इसमें `accessControlProvider` resource, action और identity context के आधार पर permission checks करता है, ताकि UI और CRUD flows केवल authorized users को उपलब्ध हों।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example access-control-permify
```

## मुख्य बिंदु

- Permify policies के साथ `accessControlProvider` integration
- resource और action level authorization checks
- navigation, buttons और CRUD pages को permission result से नियंत्रित करना
- command, provider names और URLs को original example जैसा रखना

[access-control-permify example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-permify?view=preview&theme=dark&codemirror=1)
