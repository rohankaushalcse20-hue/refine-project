<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Kinde authentication example

यह example दिखाता है कि Kinde को **Refine** application से कैसे integrate किया जाता है। `authProvider` login, logout, user identity और protected content को संभालता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-kinde
```

## मुख्य बिंदु

- Kinde authentication flow की configuration
- login state के आधार पर protected pages
- Refine application के लिए user identity उपलब्ध कराना
- resources और routes को technical example names के रूप में रखना

[auth-kinde example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
