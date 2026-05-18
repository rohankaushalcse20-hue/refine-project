<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Kinde kimlik doğrulama örneği

Bu örnek, Kinde ile kimlik doğrulama kurulumunu Refine uygulamasına bağlar. `authProvider` metotları ve örnek dizin adı korunur.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example auth-kinde
```

## Dikkat edilecek noktalar

- Kinde oturum açma ve oturum kapatma işlemleri
- Kullanıcı profilinin `getIdentity` üzerinden alınması
- Giriş gerektiren ekranlarda yönlendirme davranışı

[auth-kinde örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
