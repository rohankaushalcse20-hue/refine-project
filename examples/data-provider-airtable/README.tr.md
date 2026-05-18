<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Airtable data provider örneği

Bu örnek, Airtable kaynaklarını Refine `dataProvider` yapısıyla CRUD ekranlarına bağlamayı gösterir. Airtable tablo ve API adları çevrilmeden bırakılır.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example data-provider-airtable
```

## Dikkat edilecek noktalar

- Airtable verisinin liste, detay ve form ekranlarında kullanılması
- `dataProvider` metotlarının kaynak aksiyonlarına bağlanması
- Ortam değişkenleri ve API ayarlarının uygulamadan ayrılması

[data-provider-airtable örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-airtable?view=preview&theme=dark&codemirror=1)
