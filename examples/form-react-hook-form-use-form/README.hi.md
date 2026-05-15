<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## React Hook Form form example

यह example दिखाता है कि CRUD resources से जुड़े forms बनाने के लिए **Refine** को React Hook Form के साथ कैसे इस्तेमाल किया जाता है। Refine mutation और resource state coordinate करता है, जबकि React Hook Form fields और validation संभालता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example form-react-hook-form-use-form
```

## मुख्य बिंदु

- React Hook Form के साथ `useForm` का उपयोग
- submission को Refine mutation flow से जोड़ना
- fields और validation को form layer में रखना
- commands, URLs और APIs को code में unchanged रखना

[form-react-hook-form-use-form example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-react-hook-form-use-form?view=preview&theme=dark&codemirror=1)
