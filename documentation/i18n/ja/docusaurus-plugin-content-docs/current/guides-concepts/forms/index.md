---
title: "フォーム | Refine v5"
display_title: "フォーム"
sidebar_label: "フォーム"
description: "Refine、UI integrations、サーバー側バリデーションを使って CRUD フォームを構築します。"
---

フォームは CRUD アプリケーションの中心的な要素です。Refine は、fields、data providers、validation、mutations を結びつける hooks と components を提供します。

## 基本アプローチ

Ant Design、Material UI、Mantine、Chakra UI、React Hook Form との統合を利用できます。Refine のロジックは表示層から独立しているため、プロダクトに合った UI ライブラリを選べます。

## 作成と編集

`useForm`、`useModalForm`、`useDrawerForm`、`useStepsForm` などの hooks を使うと、作成、編集、ステップ型フォームのフローを組み立てられます。

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
});
```

## Selects と関連データ

`useSelect` は resource から options を読み込み、関連フィールド、filters、リモート検索を扱いやすくします。

## バリデーション

ローカルバリデーションとサーバーから返るエラーを組み合わせられます。多言語アプリでは、エラーメッセージを明確にし、i18n provider で翻訳しましょう。
