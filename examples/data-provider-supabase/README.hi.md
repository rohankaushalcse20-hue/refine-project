<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Supabase data provider example

यह example दिखाता है कि data provider के साथ **Refine** को Supabase से कैसे जोड़ा जाता है। Resources, lists और mutations Refine के pattern में रहते हैं, जबकि data Supabase backend से पढ़ा और लिखा जाता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example data-provider-supabase
```

## मुख्य बिंदु

- Supabase client की configuration
- CRUD resources के लिए data provider का उपयोग
- data flow को Refine core से जोड़ना
- commands, URLs और example names सुरक्षित रखना

[data-provider-supabase example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-supabase?view=preview&theme=dark&codemirror=1)
