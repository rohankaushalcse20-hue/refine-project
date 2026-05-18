<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Mantine のモーダルフォーム

この例では、**refine** の CRUD フォームを Mantine のモーダルで表示する方法を示します。新規作成や編集を短い操作で完了させたい管理画面に向いたパターンです。

## ローカルで試す

```bash
npm create refine-app@latest -- --example form-mantine-use-modal-form
```

## 主なポイント

- Mantine のモーダルをフォームの表示領域として使います。
- フォーム状態を refine の hooks と連携します。
- 保存とキャンセルの流れを resource 操作に接続します。
- CodeSandbox のリンクは元のまま保持しています。

[CodeSandbox で form-mantine-use-modal-form の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-mantine-use-modal-form?view=preview&theme=dark&codemirror=1)
