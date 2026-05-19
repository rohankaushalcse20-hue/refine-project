<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan Mantine

Contoh ini menunjukkan UI autentikasi **Refine** yang dibangun dengan Mantine. Komponen tampilan berasal dari Mantine, sedangkan login, logout, dan pemeriksaan sesi tetap mengikuti kontrak `authProvider`.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-mantine
```

## Hal yang perlu diperhatikan

- Halaman auth memakai komponen Mantine
- Proteksi route dan redirect pengguna
- Integrasi sesi dengan `authProvider`
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-mantine di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-mantine?view=preview&theme=dark&codemirror=1)
