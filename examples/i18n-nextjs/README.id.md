<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh i18n dengan Next.js

Contoh ini menunjukkan cara menggunakan **Refine** bersama Next.js dan internationalization. Refine tetap mengelola resource serta alur CRUD, sementara routing dan locale mengikuti struktur aplikasi Next.js.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example i18n-nextjs
```

## Hal yang perlu diperhatikan

- Integrasi `i18nProvider` dengan aplikasi Next.js
- Route dan locale yang tetap konsisten
- Terjemahan label menu, tombol, dan pesan feedback
- Pemisahan antara teks tampilan dan nama API seperti `resources`

[Buka contoh i18n-nextjs](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-nextjs?view=preview&theme=dark&codemirror=1)
