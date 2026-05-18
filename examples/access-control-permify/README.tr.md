<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Permify ile access control örneği

Bu örnek, Permify tabanlı izin kararlarını Refine kaynaklarına uygulayan bir erişim kontrolü akışını gösterir. `accessControlProvider`, `resources` ve örnek komutu aynen korunur.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example access-control-permify
```

## Dikkat edilecek noktalar

- Permify izin modelinin Refine aksiyonlarıyla birlikte kullanılması
- Kaynak, aksiyon ve kullanıcı bağlamının izin kararına taşınması
- Yetki sonucuna göre kullanıcı arayüzünün sadeleşmesi

[access-control-permify örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-permify?view=preview&theme=dark&codemirror=1)
