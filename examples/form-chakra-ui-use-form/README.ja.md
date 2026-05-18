<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Chakra UI の `useForm` フォーム

この例では、**refine** と Chakra UI を組み合わせて、`useForm` フックで CRUD フォームを構築する方法を示します。データ処理は refine に任せつつ、入力 UI は Chakra UI のコンポーネントで構成します。

## ローカルで試す

```bash
npm create refine-app@latest -- --example form-chakra-ui-use-form
```

## 主なポイント

- Chakra UI のフォームで `useForm` を利用します。
- 送信状態と読み込み状態を refine のフローに接続します。
- resource の作成と編集に使える基本構成です。
- 例を作成するコマンドは元のまま保持しています。

[CodeSandbox で form-chakra-ui-use-form の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-chakra-ui-use-form?view=preview&theme=dark&codemirror=1)
