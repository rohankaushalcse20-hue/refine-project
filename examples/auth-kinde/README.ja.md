<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Kinde 認証の例

この例では、Kinde を refine アプリケーションへ統合する方法を示します。`authProvider` を使って login、logout、ユーザー ID、コンテンツ保護を扱います。

## ローカルで試す

```bash
npm create refine-app@latest -- --example auth-kinde
```

## 主なポイント

- Kinde による認証フローの設定。
- login 状態に基づく protected pages。
- refine アプリケーションから利用できるユーザー ID。
- resources と routes は example の技術名として保持。

[CodeSandbox で auth-kinde の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
