<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan OTP

Contoh ini menunjukkan cara membuat alur login **Refine** berbasis one-time password. Halaman auth tetap memakai kontrak `authProvider`, sementara validasi kode OTP dipisahkan dari resource CRUD aplikasi.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-otp
```

## Hal yang perlu diperhatikan

- Alur login OTP untuk pengguna aplikasi
- Pengelolaan sesi melalui `authProvider`
- Redirect setelah autentikasi berhasil
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-otp di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-otp?view=preview&theme=dark&codemirror=1)
