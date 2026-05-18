<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Chakra UI でのサーバー側フォーム検証

この例では、サーバーから返された検証エラーを **refine** と Chakra UI のフォームに表示する方法を示します。data provider のエラー処理を保ちながら、入力欄にわかりやすく反映します。

## ローカルで試す

```bash
npm create refine-app@latest -- --example server-side-form-validation-chakra-ui
```

## 主なポイント

- サーバー側の検証エラーをフォームに表示します。
- Chakra UI の入力コンポーネントでエラー状態を扱います。
- 送信フローは refine の provider と連携します。
- CodeSandbox のリンクは元の例を保持しています。

[CodeSandbox で server-side-form-validation-chakra-ui の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/server-side-form-validation-chakra-ui?view=preview&theme=dark&codemirror=1)
