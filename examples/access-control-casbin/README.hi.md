## Casbin access control example

यह example दिखाता है कि **Refine** application में Casbin आधारित authorization कैसे जोड़ी जा सकती है। इसमें `accessControlProvider` permissions को पढ़ता है और resources पर list, create, edit और delete जैसे actions को policy के आधार पर नियंत्रित करता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example access-control-casbin
```

## मुख्य बिंदु

- Casbin policies के साथ `accessControlProvider` integration
- resource और action के अनुसार UI controls को सुरक्षित करना
- authorization checks को Refine navigation और CRUD screens से जोड़ना
- command, provider names और URLs को original example जैसा रखना

[access-control-casbin example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-casbin?view=preview&theme=dark&codemirror=1)
