<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ably live provider örneği

Bu örnek, Ably ile gerçek zamanlı güncellemeleri Refine `liveProvider` yapısına bağlamayı gösterir. Ably kanal adları ve teknik API adları çevrilmez.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example live-provider-ably
```

## Dikkat edilecek noktalar

- `liveProvider` ile abonelik ve yayınlama akışları
- Liste ekranlarında gerçek zamanlı veri yenileme
- Ably bağlantı yapılandırmasının uygulamaya aktarılması

[live-provider-ably örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/live-provider-ably?view=preview&theme=dark&codemirror=1)
