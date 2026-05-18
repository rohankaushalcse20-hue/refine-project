<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Google Login kimlik doğrulama örneği

Bu örnek, Google Login ile alınan oturum bilgisini Refine `authProvider` akışında kullanmayı gösterir. `npm create refine-app` komutu ve CodeSandbox bağlantısı aynen korunur.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example auth-google-login
```

## Dikkat edilecek noktalar

- Google hesabıyla giriş deneyimi
- Oturum bilgisinin Refine tarafında doğrulanması
- Kimlik ve yönlendirme davranışlarının `authProvider` içinde toplanması

[auth-google-login örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
