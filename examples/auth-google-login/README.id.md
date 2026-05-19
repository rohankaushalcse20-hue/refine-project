<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan Google Login

Contoh ini menunjukkan cara memakai **Refine** dengan Google Login untuk menangani sesi pengguna. `authProvider` mengelola login, logout, dan pemeriksaan akses sehingga resource CRUD tetap memakai pola Refine yang sama.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-google-login
```

## Hal yang perlu diperhatikan

- Login berbasis Google yang dibungkus oleh `authProvider`
- Penanganan status autentikasi pada route aplikasi
- Identitas pengguna tersedia untuk layout dan komponen
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-google-login di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
