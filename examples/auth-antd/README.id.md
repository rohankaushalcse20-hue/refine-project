<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan Ant Design

Contoh ini menunjukkan UI autentikasi **Refine** berbasis Ant Design. Komponen dari `@refinedev/antd` dipakai untuk halaman login dan layout, sementara `authProvider` menangani status pengguna.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-antd
```

## Hal yang perlu diperhatikan

- Halaman auth menggunakan komponen Ant Design
- Proteksi route melalui `Authenticated`
- Integrasi `authProvider` dengan layout CRUD
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-antd di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-antd?view=preview&theme=dark&codemirror=1)
