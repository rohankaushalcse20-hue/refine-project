<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Google Login authentication example

यह example दिखाता है कि **Refine** application में Google login कैसे integrate किया जा सकता है। External identity provider authentication संभालता है, और resources, routes तथा CRUD flow Refine के contract में बने रहते हैं।

## लोकल मशीन पर चलाएं

```bash
npm create refine-app@latest -- --example auth-google-login
```

## मुख्य बिंदु

- Google account के साथ login flow
- Refine application में `authProvider` का उपयोग
- authenticated content के लिए protected routes
- example names, commands और APIs को unchanged रखना

[auth-google-login example CodeSandbox में खोलें](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
