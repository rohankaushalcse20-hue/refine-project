<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Keycloak authentication example

यह example दिखाता है कि Keycloak को **Refine** application में auth provider के रूप में कैसे इस्तेमाल किया जा सकता है। Login, logout और protected pages authentication layer में रहते हैं, जबकि resources की configuration अलग और स्पष्ट रहती है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## मुख्य बिंदु

- Keycloak आधारित auth provider integration
- authenticated areas के लिए protected routes
- session handling के साथ API और variable names सुरक्षित रखना
- Keycloak roles और permissions को Refine के flow से जोड़ने की base

[auth-keycloak example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
