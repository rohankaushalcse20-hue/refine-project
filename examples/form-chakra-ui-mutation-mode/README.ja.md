<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Chakra UI の mutation mode

この例では、Chakra UI のフォームで **refine** の `mutationMode` を使う方法を示します。pessimistic、optimistic、undoable の保存体験を比較しやすい構成です。

## ローカルで試す

```bash
npm create refine-app@latest -- --example form-chakra-ui-mutation-mode
```

## 主なポイント

- フォームで `mutationMode` を設定します。
- Chakra UI のコンポーネントで保存中の状態を表現します。
- resource と provider の流れは refine のまま保ちます。
- ローカル実行用コマンドは変更していません。

[CodeSandbox で form-chakra-ui-mutation-mode の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-chakra-ui-mutation-mode?view=preview&theme=dark&codemirror=1)
