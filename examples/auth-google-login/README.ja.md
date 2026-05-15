<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Google Login 認証の例

この例では、**refine** で Google Login を使う方法を示します。主要な resources と routes を変えずに、外部 identity provider を認証フローへ統合する流れを確認できます。

## ローカルで試す

```bash
npm create refine-app@latest -- --example auth-google-login
```

## 主なポイント

- Google アカウントによるログイン。
- refine のフローで `authProvider` を利用。
- 認証済みコンテンツ向けの protected routes。
- example 名、commands、APIs はそのまま保持。

[CodeSandbox で auth-google-login の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
