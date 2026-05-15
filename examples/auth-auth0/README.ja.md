<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Auth0 認証の例

この例では、**refine** を Auth0 のログインフローに接続する方法を示します。ユーザー ID は Auth0 provider が管理しつつ、アプリケーション側では refine の resources と providers をそのまま利用できます。

## ローカルで試す

```bash
npm create refine-app@latest -- --example auth-auth0
```

## 主なポイント

- Auth0 と `authProvider` の連携。
- 認証済み routes と resources の保護。
- refine の構成を保ちながら外部ログインフローを利用。
- example 名、commands、URLs は元の例と同じまま保持。

[CodeSandbox で auth-auth0 の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
