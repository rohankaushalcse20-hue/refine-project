<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan Kinde

Contoh ini menunjukkan cara memakai **Refine** bersama Kinde untuk alur autentikasi aplikasi web. `authProvider` menghubungkan sesi Kinde dengan pemeriksaan akses, redirect, dan identitas pengguna di Refine.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-kinde
```

## Hal yang perlu diperhatikan

- Login dan logout melalui Kinde
- Status autentikasi yang digunakan oleh route Refine
- Pengembalian identitas pengguna melalui `getIdentity`
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-kinde di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
