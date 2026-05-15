<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Keycloak 認証の例

この例では、refine アプリケーションで Keycloak を auth provider として使う方法を示します。resources の設定を認証レイヤーから分けたまま、login、logout、ページ保護の流れを扱います。

## ローカルで試す

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## 主なポイント

- Keycloak ベースの auth provider 連携。
- 認証済み領域向けの protected routes。
- API 名や example 変数名を変えずに session を扱う。
- Keycloak の roles と permissions を refine へ適用するための土台。

[CodeSandbox で auth-keycloak の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
