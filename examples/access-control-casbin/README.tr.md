<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Casbin ile access control örneği

Bu örnek, Casbin kurallarını Refine uygulamasındaki kaynak ve aksiyon izinlerine bağlamayı gösterir. `accessControlProvider`, `can` kontrolü ve `resources` adları özgün haliyle korunur.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example access-control-casbin
```

## Dikkat edilecek noktalar

- Casbin izin modelinin Refine aksiyonlarına eşlenmesi
- Listeleme, oluşturma, düzenleme ve silme ekranlarında yetki kontrolü
- Menü ve sayfa görünürlüğünün izin sonucuna göre değişmesi

[access-control-casbin örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-casbin?view=preview&theme=dark&codemirror=1)
