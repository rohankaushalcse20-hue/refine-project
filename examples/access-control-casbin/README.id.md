<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh access control dengan Casbin

Contoh ini menunjukkan cara memakai **Refine** bersama Casbin untuk menerapkan izin pada `resources`, actions, dan route. Logika otorisasi tetap terpisah dari UI, sementara `accessControlProvider` menentukan apa yang dapat dilihat atau diubah pengguna.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example access-control-casbin
```

## Hal yang perlu diperhatikan

- Integrasi Casbin melalui `accessControlProvider`
- Aturan otorisasi yang dapat dipakai ulang untuk action CRUD
- Layar terlindungi tanpa mengubah nama `resources` Refine
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh access-control-casbin di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-casbin?view=preview&theme=dark&codemirror=1)
