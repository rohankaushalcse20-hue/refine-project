## Sanity data provider example

यह example **Refine** में Sanity data provider के साथ content-backed CRUD application बनाना दिखाता है। इसमें Sanity dataset से records पढ़ना और Refine resources के जरिए उन्हें manage करना शामिल है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example data-provider-sanity
```

## मुख्य बिंदु

- Sanity data provider को Refine resource layer से जोड़ना
- content records के लिए list, create और edit flows
- data fetching hooks को Sanity client configuration से चलाना
- commands, URLs और provider names को original example जैसा रखना

[data-provider-sanity example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-sanity?view=preview&theme=dark&codemirror=1)
