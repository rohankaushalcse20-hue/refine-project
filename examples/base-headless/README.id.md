<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh dasar headless

Contoh ini menunjukkan aplikasi **Refine** dasar tanpa library UI bawaan. Pendekatan headless memberi kendali penuh atas markup dan styling, sementara hooks Refine tetap menangani resource dan operasi CRUD.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example base-headless
```

## Hal yang perlu diperhatikan

- Fondasi Refine tanpa ketergantungan UI framework
- Hooks data dan resource tetap memakai API Refine
- Cocok untuk desain UI yang sepenuhnya kustom
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh base-headless di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/base-headless?view=preview&theme=dark&codemirror=1)
