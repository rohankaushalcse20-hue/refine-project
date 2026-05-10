<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## React 向け i18n サンプル

この example では、**Refine** を React アプリケーションで国際化と一緒に使う方法を示します。CRUD ロジックは Refine に残したまま、翻訳は適切な provider を通して追加します。

## ローカルで実行する

```bash
npm create refine-app@latest -- --example i18n-react
```

## 確認ポイント

- `i18nProvider` の設定
- UI 上での言語切り替え
- menus、actions、表示テキストの翻訳
- code 内の resources、routes、APIs がそのまま保たれていること

[i18n-react example を開く](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-react?view=preview&theme=dark&codemirror=1)
