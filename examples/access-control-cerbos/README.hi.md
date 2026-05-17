## Cerbos access control example

यह example बताता है कि **Refine** में Cerbos policy engine के साथ authorization decisions कैसे लिए जा सकते हैं। Application `accessControlProvider` के जरिए Cerbos से permission पूछती है और allowed actions के अनुसार pages और buttons दिखाती है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example access-control-cerbos
```

## मुख्य बिंदु

- Cerbos policies से Refine resource permissions नियंत्रित करना
- `can` checks के आधार पर create, edit और delete actions सीमित करना
- authorization logic को UI layer से अलग रखना
- commands, resource names और provider API को original example जैसा रखना

[access-control-cerbos example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-cerbos?view=preview&theme=dark&codemirror=1)
