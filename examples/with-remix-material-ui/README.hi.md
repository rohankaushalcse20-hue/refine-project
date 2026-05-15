<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Remix with Material UI example

यह example दिखाता है कि Material UI का उपयोग करते हुए Remix application में **Refine** कैसे चलाया जाता है। यह Remix routing को Refine resources, providers और Material UI visual components के साथ जोड़ता है।

> ⚠️ **Known Incompatibility:** यह example अभी MUI X v8 के साथ incompatible है। Vite के बिना Remix Node.js पर चलता है, जो npm packages से आने वाले CSS imports parse नहीं कर सकता। MUI X v8 CSS files export करता है, जिससे runtime पर `SyntaxError: Unexpected token '.'` errors आते हैं। Full MUI X v8 support के लिए [Remix + Vite](https://remix.run/docs/en/main/guides/vite) पर migrate करने पर विचार करें।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example with-remix-material-ui
```

## मुख्य बिंदु

- Remix और Refine integration
- Material UI के साथ layout और components
- framework flow में resources और routes को सुरक्षित रखना
- commands और links को local reproduction के लिए unchanged रखना

[with-remix-material-ui example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/with-remix-material-ui?view=preview&theme=dark&codemirror=1)
