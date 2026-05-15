<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Auth0 authentication example

यह example दिखाता है कि **Refine** को Auth0 login flow से कैसे जोड़ा जा सकता है। Application Refine के resources और providers का उपयोग करती रहती है, जबकि user identity Auth0 provider संभालता है।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-auth0
```

## मुख्य बिंदु

- Auth0 के साथ `authProvider` integration
- protected routes और authenticated resources
- external login flow के साथ Refine की structure सुरक्षित रखना
- commands, URLs और API names को original example जैसा रखना

[auth-auth0 example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
