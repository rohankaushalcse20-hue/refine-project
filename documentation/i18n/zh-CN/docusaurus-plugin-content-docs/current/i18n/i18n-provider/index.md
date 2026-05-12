---
title: "I18n Provider | Refine v5"
display_title: "I18n Provider"
sidebar_label: "I18n Provider"
description: "使用 `i18nProvider` 将 Refine 接入你选择的翻译库。"
---

Refine 不强制绑定特定翻译库。你可以通过 `i18nProvider` 接入 `react-i18next`、`next-i18next`，或自定义实现的本地化方案。

## 基础接口

```tsx
const i18nProvider = {
  translate: (key, options, defaultMessage) => defaultMessage ?? key,
  changeLocale: (lang) => Promise.resolve(lang),
  getLocale: () => "zh-CN",
};
```

把 provider 传给 `<Refine />` 后，hooks、menus、buttons 与 components 就可以使用统一的翻译函数。

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

## Hooks

通过 `useTranslate` 获取 `translate` 函数，通过 `useSetLocale` 切换语言，通过 `useGetLocale` 读取当前 locale。

## 建议

保持 keys 稳定，不要翻译技术标识符，并使用真实数据验证长文本、复数、日期与货币格式在各 locale 下的显示效果。
