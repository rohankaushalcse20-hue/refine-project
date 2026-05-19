<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Contoh autentikasi headless

Contoh ini menunjukkan alur autentikasi **Refine** tanpa terikat pada library UI tertentu. Aplikasi dapat mengatur tampilan sendiri, sementara `authProvider` tetap menyediakan login, logout, dan pemeriksaan sesi.

## Menjalankan secara lokal

```bash
npm create refine-app@latest -- --example auth-headless
```

## Hal yang perlu diperhatikan

- Pola autentikasi headless untuk UI kustom
- Penggunaan `Authenticated` untuk proteksi route
- Kontrak `authProvider` tetap menjadi pusat logika sesi
- Command, URL, dan nama teknis tetap dipertahankan tanpa diterjemahkan

[Buka contoh auth-headless di CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-headless?view=preview&theme=dark&codemirror=1)
