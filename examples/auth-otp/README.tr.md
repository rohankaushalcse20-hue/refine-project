<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## OTP kimlik doğrulama örneği

Bu örnek, tek kullanımlık parola tabanlı giriş deneyimini Refine `authProvider` yapısıyla gösterir. OTP kısaltması, komut ve bağlantılar çevrilmeden bırakılmıştır.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example auth-otp
```

## Dikkat edilecek noktalar

- OTP kodu ile giriş akışı
- Oturum kontrolünün `check` metodunda ele alınması
- Giriş sonrası kullanıcıyı uygulama kaynaklarına yönlendirme

[auth-otp örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-otp?view=preview&theme=dark&codemirror=1)
