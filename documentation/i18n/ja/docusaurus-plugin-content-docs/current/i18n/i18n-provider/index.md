---
title: "I18n Provider | Refine v5"
display_title: "I18n Provider"
sidebar_label: "I18n Provider"
description: "i18nProvider を使って、Refine を好みの翻訳ライブラリへ接続します。"
---

Refine は翻訳ライブラリを固定しません。代わりに `i18nProvider` を通して、`react-i18next`、`next-i18next`、あるいは独自実装を接続できます。

## 基本インターフェース

```tsx
const i18nProvider = {
  translate: (key, options, defaultMessage) => defaultMessage ?? key,
  changeLocale: (lang) => Promise.resolve(lang),
  getLocale: () => "ja",
};
```

provider を `<Refine />` に渡すと、hooks、menus、buttons、components が翻訳を参照できるようになります。

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

## Hooks

`useTranslate` で `translate` 関数を取得し、`useSetLocale` で言語を切り替え、`useGetLocale` で現在の locale を確認できます。

## 推奨事項

keys は安定したまま維持し、技術的な識別子は翻訳せず、実データで各 locale を確認して長文、複数形、日付や通貨の表記を検証しましょう。
