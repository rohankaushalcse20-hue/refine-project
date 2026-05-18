<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Auth0 kimlik doğrulama örneği

Bu örnek, Auth0 oturum açma akışını Refine `authProvider` yapısıyla birleştirir. Komutlar, URL'ler ve sağlayıcı adları teknik doğruluk için çevrilmeden bırakılmıştır.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example auth-auth0
```

## Dikkat edilecek noktalar

- Auth0 ile giriş ve çıkış işlemleri
- `check`, `login`, `logout` ve `getIdentity` davranışları
- Korunan sayfalarda oturum durumunun kullanılması

[auth-auth0 örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
