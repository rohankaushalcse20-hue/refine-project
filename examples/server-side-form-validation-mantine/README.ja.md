<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Mantine でのサーバー側フォーム検証

この例では、サーバーから返された検証エラーを **refine** と Mantine のフォームに反映する方法を示します。data provider のエラーを入力欄のメッセージとして扱う流れを確認できます。

## ローカルで試す

```bash
npm create refine-app@latest -- --example server-side-form-validation-mantine
```

## 主なポイント

- サーバー側の検証エラーをフォーム項目に表示します。
- Mantine のコンポーネントでエラー表示を整えます。
- 送信とエラー処理は refine の流れに接続します。
- CodeSandbox の URL は変更していません。

[CodeSandbox で server-side-form-validation-mantine の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/server-side-form-validation-mantine?view=preview&theme=dark&codemirror=1)
