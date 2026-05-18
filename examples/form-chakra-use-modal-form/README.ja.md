<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Chakra UI のモーダルフォーム

この例では、**refine** の CRUD フォームを Chakra UI のモーダル内で開く方法を示します。一覧画面の文脈を保ったまま、新規作成や編集を行いたい場合に向いています。

## ローカルで試す

```bash
npm create refine-app@latest -- --example form-chakra-use-modal-form
```

## 主なポイント

- Chakra UI のモーダルをフォームの表示先として使います。
- モーダルの開閉状態を refine のフォームフローと合わせます。
- resource の作成と編集を画面遷移なしで扱います。
- CodeSandbox の URL は元の例を指したままです。

[CodeSandbox で form-chakra-use-modal-form の例を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-chakra-use-modal-form?view=preview&theme=dark&codemirror=1)
