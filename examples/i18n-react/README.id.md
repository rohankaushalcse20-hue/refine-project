<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh i18n dengan React

Contoh ini menunjukkan cara memakai **Refine** di aplikasi React dengan dukungan internationalization. Refine menangani logika CRUD, sementara teks terjemahan berasal dari `i18nProvider` yang sesuai.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example i18n-react
```

## Hal yang perlu diperhatikan

- Konfigurasi `i18nProvider`
- Pergantian bahasa dari UI
- Terjemahan menu, actions, dan teks yang terlihat pengguna
- `resources`, `routes`, dan API tetap memakai nama aslinya

[Buka contoh i18n-react](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-react?view=preview&theme=dark&codemirror=1)
