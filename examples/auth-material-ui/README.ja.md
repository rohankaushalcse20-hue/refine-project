<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Material UI 認証の例

この例では、Material UI ベースの React アプリケーションで **refine** の認証フローを使う方法を示します。CRUD の構造は refine が管理し、画面と visual components は Material UI 連携を使います。

## ローカルで試す

```bash
npm create refine-app@latest -- --example auth-material-ui
```

## 主なポイント

- `authProvider` の設定。
- 認証済み resources 向けの protected routes。
- Material UI による layout と forms。
- resources、commands、APIs はコード内でそのまま保持。

[CodeSandbox で auth-material-ui の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-material-ui?view=preview&theme=dark&codemirror=1)
