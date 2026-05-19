<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan Auth0

Contoh ini menunjukkan cara memakai **Refine** dengan Auth0 sebagai penyedia autentikasi. Alur login, logout, pengecekan sesi, dan identitas pengguna dihubungkan melalui `authProvider` tanpa mengubah API Refine.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-auth0
```

## Hal yang perlu diperhatikan

- Integrasi Auth0 melalui `authProvider`
- Proteksi halaman dengan status autentikasi
- Pengambilan identitas pengguna untuk UI aplikasi
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-auth0 di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
