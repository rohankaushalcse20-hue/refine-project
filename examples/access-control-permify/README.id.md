<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh access control dengan Permify

Contoh ini menunjukkan cara memakai **Refine** dengan Permify untuk memeriksa izin berbasis relasi. Aplikasi tetap memakai pola CRUD Refine, sementara keputusan akses didelegasikan ke `accessControlProvider`.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example access-control-permify
```

## Hal yang perlu diperhatikan

- Integrasi Permify untuk model izin berbasis relasi
- Guard UI dan route yang membaca hasil `can`
- Nama resource, action, dan provider tetap memakai identifier asli
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh access-control-permify di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-permify?view=preview&theme=dark&codemirror=1)
