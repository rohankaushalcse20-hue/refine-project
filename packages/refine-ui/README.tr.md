# registry-template

Kendi component registry'nizi çalıştırmak için `shadcn` CLI kullanabilirsiniz. Kendi registry'niz; custom components, hooks, pages ve diğer dosyaları herhangi bir React projesine dağıtmanıza yardımcı olur.

> [!IMPORTANT]
> Bu template Tailwind v4 kullanır. Tailwind v3 için [registry-template](https://github.com/shadcn-ui/registry-template) sayfasına bakın.

## Getting Started

Bu template, Next.js ile custom registry oluşturmak için hazırlanmıştır.

- Template, component'leri ve dosyalarını tanımlamak için `registry.json` dosyasını kullanır.
- Registry build etmek için `shadcn build` komutu kullanılır.
- Registry items, `public/r/[name].json` altında static files olarak servis edilir.
- Template, registry items servis etmek için route handler da içerir.
- Her registry item `shadcn` CLI ile uyumludur.
- `Open in v0` api kullanılarak v0 entegrasyonu da eklenmiştir.

## Dokümantasyon

Tam dokümantasyon için [shadcn dokümantasyonunu](https://ui.shadcn.com/docs/registry) ziyaret edin.
