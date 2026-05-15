# registry-template template

`shadcn` CLI を使うと、独自の component registry を実行できます。独自 registry を持つことで、components、hooks、pages、その他のカスタムファイルを任意の React プロジェクトへ配布できます。

> [!IMPORTANT]
> この template は Tailwind v4 を使用します。Tailwind v3 については [registry-template](https://github.com/shadcn-ui/registry-template) を参照してください。

## はじめる

これは Next.js でカスタム registry を作成するための template です。

- template は `registry.json` で components と関連ファイルを定義します。
- `shadcn build` コマンドで registry を build します。
- registry items は `public/r/[name].json` の static files として配信されます。
- registry items を配信する route handler も含まれています。
- すべての registry items は `shadcn` CLI と互換性があります。
- `Open in v0` API との連携も含まれています。

## ドキュメント

完全なドキュメントは [shadcn の registry ドキュメント](https://ui.shadcn.com/docs/registry)を参照してください。
