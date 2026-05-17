## Audit log provider example

यह example दिखाता है कि **Refine** में `auditLogProvider` का उपयोग करके user actions को track कैसे किया जा सकता है। CRUD operations के दौरान create, update और delete events record होते हैं ताकि activity history review की जा सके।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example audit-log-provider
```

## मुख्य बिंदु

- `auditLogProvider` के साथ mutation events capture करना
- resource, action और user context को audit entries में रखना
- admin workflows में activity trail दिखाने का pattern
- commands और provider method names को original example जैसा रखना

[audit-log-provider example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/audit-log-provider?view=preview&theme=dark&codemirror=1)
