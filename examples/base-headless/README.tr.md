<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Headless temel örneği

Bu örnek, Refine'ın headless yapısını kullanarak arayüz kütüphanesine bağlı kalmadan temel CRUD akışının nasıl kurulacağını gösterir. Görsel katman bilinçli olarak sade tutulur.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example base-headless
```

## Dikkat edilecek noktalar

- UI framework zorunluluğu olmadan Refine çekirdek akışı
- Listeleme, oluşturma ve düzenleme için temel kaynak yapısı
- `Refine`, `resources` ve provider adları teknik biçimleriyle korunur

[base-headless örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/base-headless?view=preview&theme=dark&codemirror=1)
