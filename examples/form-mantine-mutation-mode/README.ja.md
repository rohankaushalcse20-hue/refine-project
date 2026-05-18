<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Mantine の mutation mode

この例では、Mantine のフォームで **refine** の `mutationMode` を使う方法を示します。保存時の pessimistic、optimistic、undoable の違いを UI で確認できます。

## ローカルで試す

```bash
npm create refine-app@latest -- --example form-mantine-mutation-mode
```

## 主なポイント

- Mantine フォームで `mutationMode` を設定します。
- データ更新中のフィードバックを画面に反映します。
- resource と provider の処理は refine に任せます。
- ローカル実行用コマンドは元のままです。

[CodeSandbox で form-mantine-mutation-mode の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-mantine-mutation-mode?view=preview&theme=dark&codemirror=1)
