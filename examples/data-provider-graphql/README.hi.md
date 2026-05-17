## GraphQL data provider example

यह example **Refine** में GraphQL data provider के साथ CRUD operations चलाना दिखाता है। Application resources को GraphQL queries और mutations से जोड़ती है ताकि list, create, edit और delete workflows काम कर सकें।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example data-provider-graphql
```

## मुख्य बिंदु

- GraphQL data provider के साथ Refine resources
- queries और mutations के जरिए CRUD operations
- data fetching hooks को GraphQL backend से जोड़ना
- commands, URLs और provider names को original example जैसा रखना

[data-provider-graphql example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-graphql?view=preview&theme=dark&codemirror=1)
