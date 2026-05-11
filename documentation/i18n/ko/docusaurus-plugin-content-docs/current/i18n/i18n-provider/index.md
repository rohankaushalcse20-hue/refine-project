---
title: "I18n Provider | Refine v5"
display_title: "I18n Provider"
sidebar_label: "I18n Provider"
description: "`i18nProvider`를 사용해 Refine를 원하는 번역 라이브러리와 연결합니다."
---

Refine는 특정 번역 라이브러리를 강제하지 않습니다. 대신 `i18nProvider`를 통해 `react-i18next`, `next-i18next`, 또는 자체 구현한 솔루션을 연결할 수 있습니다.

## 기본 인터페이스

```tsx
const i18nProvider = {
  translate: (key, options, defaultMessage) => defaultMessage ?? key,
  changeLocale: (lang) => Promise.resolve(lang),
  getLocale: () => "ko",
};
```

provider를 `<Refine />`에 전달하면 hooks, menus, buttons, components가 번역 함수를 사용할 수 있게 됩니다.

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

## Hooks

`useTranslate`로 `translate` 함수를 가져오고, `useSetLocale`로 언어를 바꾸고, `useGetLocale`로 현재 locale을 확인할 수 있습니다.

## 권장 사항

keys는 안정적으로 유지하고 기술적 식별자는 번역하지 말고, 실제 데이터로 각 locale을 검증해 긴 문장, 복수형, 날짜 및 통화 형식을 확인하세요.
