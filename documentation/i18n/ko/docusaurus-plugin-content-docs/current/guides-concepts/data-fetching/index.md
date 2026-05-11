---
title: "데이터 가져오기 | Refine v5"
display_title: "데이터 가져오기"
sidebar_label: "데이터 가져오기"
description: "data providers와 hooks를 통해 Refine가 UI와 API를 연결하는 방식을 배웁니다."
---

관리형 애플리케이션에서는 데이터가 핵심입니다. Refine는 [`DataProvider`](/core/docs/core/interface-references#dataprovider) 인터페이스를 구현한 `dataProvider`를 통해 UI를 하나 이상의 데이터 소스에 연결합니다.

data provider는 `resource`, `id`, `meta` 같은 정보를 받아 올바른 API endpoint를 호출합니다.

## 데이터 hooks

data provider를 등록하면 `useList`, `useOne`, `useCreate`, `useUpdate`, `useDelete` 같은 hooks로 CRUD 작업을 처리할 수 있습니다.

```tsx
import { useOne } from "@refinedev/core";

const Product = () => {
  const { data, isLoading } = useOne({
    resource: "products",
    id: 1,
  });

  if (isLoading) return <span>Loading...</span>;
  return <pre>{JSON.stringify(data, null, 2)}</pre>;
};
```

## 상태와 캐시

데이터 hooks 내부에는 TanStack Query가 사용됩니다. 이를 통해 로딩, 오류, 성공 상태와 캐시, request 중복 제거, 자동 invalidation, optimistic update를 활용할 수 있습니다.

## 여러 providers

resource마다 다른 provider를 지정할 수도 있습니다. 예를 들어 `posts`는 REST, `users`는 GraphQL을 사용하더라도 components 입장에서는 동일한 API를 유지할 수 있습니다.
