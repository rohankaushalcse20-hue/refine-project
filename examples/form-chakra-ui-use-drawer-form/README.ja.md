<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Chakra UI の drawer フォーム

この例では、**refine** のフォームを Chakra UI の drawer 内に表示する構成を示します。一覧を表示したまま、横から開くパネルでレコードを編集する管理画面に適しています。

## ローカルで試す

```bash
npm create refine-app@latest -- --example form-chakra-ui-use-drawer-form
```

## 主なポイント

- Chakra UI の drawer をフォームのコンテナとして利用します。
- 保存、キャンセル、読み込み状態を refine の hooks と連携します。
- resource の編集をサイドパネルで行うための土台になります。
- コマンドとリンクは元の例と同じです。

[CodeSandbox で form-chakra-ui-use-drawer-form の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-chakra-ui-use-drawer-form?view=preview&theme=dark&codemirror=1)
