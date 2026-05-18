<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Strapi v4 data provider örneği

Bu örnek, Strapi v4 içerik API'sini Refine CRUD akışına bağlamayı gösterir. Strapi koleksiyonları, API adları ve komutlar çevrilmeden bırakılır.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example data-provider-strapi-v4
```

## Dikkat edilecek noktalar

- Strapi v4 kaynaklarının Refine ekranlarında kullanılması
- Kimlik doğrulama ve API yapılandırmasının ayrılması
- Listeleme, detay ve form işlemlerinin `dataProvider` üzerinden çalışması

[data-provider-strapi-v4 örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-strapi-v4?view=preview&theme=dark&codemirror=1)
