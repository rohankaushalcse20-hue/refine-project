---
title: "테이블과 목록 | Refine v5"
display_title: "테이블"
sidebar_label: "테이블"
description: "Refine로 tables, lists, filters, sorting, pagination을 구성하는 방법을 설명합니다."
---

테이블과 목록은 API 데이터를 탐색하기 쉬운 UI로 바꿔 줍니다. Refine에는 pagination, filters, sorting, loading state를 data provider와 연결하는 hooks가 준비되어 있습니다.

## 목록 표시

`useTable`과 `useList`는 목록 화면의 기본입니다. UI integration과 함께 써도 되고, 자체 components와 함께 써도 됩니다.

```tsx
const table = useTable({
  resource: "products",
  pagination: { pageSize: 10 },
});
```

## 필터와 정렬

filters와 sorters는 data provider가 API에 전달할 수 있는 파라미터로 변환됩니다. 덕분에 UI와 backend 통신의 결합도를 낮출 수 있습니다.

## CRUD actions

목록에 create, edit, show, delete buttons를 조합할 수 있습니다. actions는 access control provider의 권한을 존중하고 labels는 i18n으로 번역할 수 있습니다.

## 사용자 경험

로딩, 빈 상태, 오류 상태를 분명하게 보여 주세요. 큰 테이블에서는 pagination이나 점진적 로딩을 사용해 UI 반응성을 유지하는 것이 좋습니다.
