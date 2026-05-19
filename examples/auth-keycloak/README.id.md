<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan Keycloak

Contoh ini menunjukkan cara menghubungkan **Refine** ke Keycloak untuk autentikasi aplikasi admin. Integrasi `authProvider` menjaga alur login dan pemeriksaan izin tetap dekat dengan lifecycle Refine.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## Hal yang perlu diperhatikan

- Konfigurasi Keycloak untuk aplikasi Refine
- Login, logout, dan validasi sesi melalui `authProvider`
- Route terlindungi untuk halaman CRUD
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-keycloak di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
