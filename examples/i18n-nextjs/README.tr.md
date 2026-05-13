<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Next.js ile i18n örneği

Bu örnek, **Refine** ile Next.js ve internationalization kullanımını gösterir. Refine resource ve CRUD akışlarını yönetmeye devam eder; routing ve locale yapısı ise Next.js uygulamasının düzenini izler.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example i18n-nextjs
```

## Dikkat edilecek noktalar

- `i18nProvider` entegrasyonunun Next.js uygulamasıyla uyumu
- Route ve locale yapısının tutarlı kalması
- Menü etiketleri, butonlar ve feedback mesajlarının çevirileri
- Görünen metinler ile `resources` gibi API adlarının ayrılması

[i18n-nextjs örneğini aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-nextjs?view=preview&theme=dark&codemirror=1)
