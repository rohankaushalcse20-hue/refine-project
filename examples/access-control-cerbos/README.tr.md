<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Cerbos ile access control örneği

Bu örnek, Cerbos politika kararlarını Refine `accessControlProvider` akışına dahil etmeyi gösterir. Kullanıcıya görünen metinler Türkçedir; API adları ve örnek kimliği değiştirilmemiştir.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example access-control-cerbos
```

## Dikkat edilecek noktalar

- Cerbos kararlarının `can` sonucu olarak uygulanması
- Kaynak bazlı aksiyon izinleri
- Yetkisiz durumlarda buton ve sayfa davranışları

[access-control-cerbos örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-cerbos?view=preview&theme=dark&codemirror=1)
