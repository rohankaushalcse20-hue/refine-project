<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Keycloak kimlik doğrulama örneği

Bu örnek, Keycloak oturum yönetimini Refine `authProvider` sözleşmesiyle kullanmayı gösterir. Keycloak, React ve Refine adları teknik ad olarak bırakılmıştır.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## Dikkat edilecek noktalar

- Keycloak giriş ve çıkış akışları
- Korunan rotalarda oturum kontrolü
- Kullanıcı bilgisinin Refine bileşenlerinde tüketilmesi

[auth-keycloak örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
