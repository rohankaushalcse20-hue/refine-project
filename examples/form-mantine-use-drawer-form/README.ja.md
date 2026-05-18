<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Mantine の drawer フォーム

この例では、Mantine の drawer 内で **refine** のフォームを扱う方法を示します。一覧画面の横に編集パネルを開き、文脈を失わずにレコードを更新できます。

## ローカルで試す

```bash
npm create refine-app@latest -- --example form-mantine-use-drawer-form
```

## 主なポイント

- Mantine の drawer を編集フォームに利用します。
- refine のフォーム hooks で保存処理を管理します。
- resource の作成と更新をサイドパネルから実行します。
- 例の作成コマンドは変更していません。

[CodeSandbox で form-mantine-use-drawer-form の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-mantine-use-drawer-form?view=preview&theme=dark&codemirror=1)
