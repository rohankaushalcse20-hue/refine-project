<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan Material UI

Contoh ini menunjukkan halaman autentikasi **Refine** berbasis Material UI. Layout dan form menggunakan komponen Material UI, sementara `authProvider` menjaga perilaku login dan status pengguna tetap konsisten.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-material-ui
```

## Hal yang perlu diperhatikan

- Komponen Material UI untuk halaman login
- Proteksi route dengan status autentikasi
- Integrasi `authProvider` dengan resource CRUD
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-material-ui di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-material-ui?view=preview&theme=dark&codemirror=1)
