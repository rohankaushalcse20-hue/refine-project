<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Hasura data provider example

यह example दिखाता है कि Hasura के साथ **Refine** कैसे इस्तेमाल किया जाता है। Refine resources Hasura की GraphQL API से जुड़ते हैं, और queries तथा mutations core flow के अंदर रहती हैं।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example data-provider-hasura
```

## मुख्य बिंदु

- Hasura और GraphQL integration
- CRUD resources को data provider से जोड़ना
- lists, filters और mutations को Refine के माध्यम से चलाना
- original example के commands और URLs सुरक्षित रखना

[data-provider-hasura example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-hasura?view=preview&theme=dark&codemirror=1)
