## Strapi V4 auth/data provider example

यह example **Refine** में Strapi V4 auth और data provider को साथ में इस्तेमाल करना दिखाता है। इसमें authentication, resource data fetching और CRUD screens को Strapi backend से जोड़ने का starter flow शामिल है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example data-provider-strapi-v4
```

## मुख्य बिंदु

- Strapi V4 backend के साथ `authProvider` और data provider setup
- login state, protected resources और CRUD operations की wiring
- list/create/edit screens को Strapi API से जोड़ना
- commands, URLs और provider names को original example जैसा रखना

[data-provider-strapi-v4 example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-strapi-v4?view=preview&theme=dark&codemirror=1)
