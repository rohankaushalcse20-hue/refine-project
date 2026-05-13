<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## React ile i18n örneği

Bu örnek, internationalization desteği olan bir React uygulamasında **Refine** kullanımını gösterir. Refine CRUD mantığını yönetir; çeviri metinleri ise uygun `i18nProvider` üzerinden gelir.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example i18n-react
```

## Dikkat edilecek noktalar

- `i18nProvider` yapılandırması
- UI üzerinden dil değiştirme
- Menü, actions ve kullanıcıya görünen metinlerin çevirileri
- `resources`, `routes` ve API adlarının özgün kalması

[i18n-react örneğini aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-react?view=preview&theme=dark&codemirror=1)
