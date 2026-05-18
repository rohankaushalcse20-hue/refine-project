<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Mantine の `useForm` フォーム

この例では、**refine** と Mantine を使って `useForm` ベースの CRUD フォームを作成する方法を示します。refine のデータフローと Mantine のフォーム UI を組み合わせた構成です。

## ローカルで試す

```bash
npm create refine-app@latest -- --example form-mantine-use-form
```

## 主なポイント

- Mantine のフォームで `useForm` を利用します。
- resource の作成と編集を refine の hooks に接続します。
- 送信中や読み込み中の状態を UI に反映します。
- コマンドは元の README と同じです。

[CodeSandbox で form-mantine-use-form の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-mantine-use-form?view=preview&theme=dark&codemirror=1)
