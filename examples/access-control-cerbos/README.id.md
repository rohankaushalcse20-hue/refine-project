<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh access control dengan Cerbos

Contoh ini menunjukkan cara menghubungkan **Refine** dengan Cerbos untuk mengevaluasi policy otorisasi di luar aplikasi React. `accessControlProvider` meneruskan konteks pengguna, resource, dan action agar keputusan izin tetap konsisten.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example access-control-cerbos
```

## Hal yang perlu diperhatikan

- Pemeriksaan izin melalui policy Cerbos
- Pemisahan aturan otorisasi dari komponen UI
- Proteksi route dan action CRUD melalui `accessControlProvider`
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh access-control-cerbos di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-cerbos?view=preview&theme=dark&codemirror=1)
