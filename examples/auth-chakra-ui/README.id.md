<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi dengan Chakra UI

Contoh ini menunjukkan cara membangun halaman autentikasi **Refine** dengan Chakra UI. Integrasi UI tetap terpisah dari `authProvider`, sehingga logika sesi dan tampilan dapat dirawat secara mandiri.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-chakra-ui
```

## Hal yang perlu diperhatikan

- Komponen Chakra UI untuk halaman auth
- Pemeriksaan sesi melalui `authProvider`
- Route terlindungi untuk halaman CRUD
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-chakra-ui di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-chakra-ui?view=preview&theme=dark&codemirror=1)
