<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Hasura data provider örneği

Bu örnek, Hasura GraphQL API'sini Refine veri katmanına bağlar. GraphQL, Hasura ve `dataProvider` adları teknik kullanım için çevrilmeden korunur.

## Lokal çalıştırma

```bash
npm create refine-app@latest -- --example data-provider-hasura
```

## Dikkat edilecek noktalar

- Hasura GraphQL sorgularıyla kaynak verisi okuma
- CRUD aksiyonlarının Refine veri sağlayıcısına yönlenmesi
- API uç noktası ve yetkilendirme ayarlarının yapılandırılması

[data-provider-hasura örneğini CodeSandbox'da aç](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-hasura?view=preview&theme=dark&codemirror=1)
