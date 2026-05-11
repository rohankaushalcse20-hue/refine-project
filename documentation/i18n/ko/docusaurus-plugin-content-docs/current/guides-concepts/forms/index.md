---
title: "폼 | Refine v5"
display_title: "폼"
sidebar_label: "폼"
description: "Refine, UI integrations, 서버 검증을 활용해 CRUD 폼을 구성합니다."
---

폼은 CRUD 애플리케이션의 핵심 요소입니다. Refine는 fields, data providers, validation, mutations를 연결하는 hooks와 components를 제공합니다.

## 기본 접근 방식

Ant Design, Material UI, Mantine, Chakra UI, React Hook Form 통합을 사용할 수 있습니다. Refine의 로직은 표현 계층과 분리되어 있으므로 제품에 맞는 UI 라이브러리를 자유롭게 선택할 수 있습니다.

## 생성과 수정

`useForm`, `useModalForm`, `useDrawerForm`, `useStepsForm` 같은 hooks를 이용해 생성, 수정, 단계형 폼 흐름을 구성할 수 있습니다.

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
});
```

## Select와 연관 데이터

`useSelect`는 resource에서 options를 불러와 관계형 필드, filters, 원격 검색을 다루기 쉽게 만듭니다.

## 검증

로컬 검증과 서버 오류를 함께 사용할 수 있습니다. 다국어 애플리케이션이라면 오류 메시지를 명확하게 유지하고 i18n provider를 통해 번역하세요.
