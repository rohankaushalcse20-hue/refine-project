---
title: "기본 개념 | Refine v5"
display_title: "기본 개념"
sidebar_label: "기본 개념"
description: "Refine의 headless 아키텍처, resources, providers, hooks, meta 개념을 이해합니다."
---

Refine는 웹 애플리케이션을 빠르게 구축하기 위한 확장성 높은 프레임워크입니다. **hooks**, 교체 가능한 **providers**, 안정적인 데이터 및 상태 관리가 핵심 기반입니다.

## Headless 개념

Refine는 특정 스타일의 컴포넌트 세트에 묶어 두지 않습니다. 대신 `hooks`, `components`, `providers`, 유틸리티를 제공하고 비즈니스 로직과 UI를 분리합니다.

이 덕분에 자체 디자인 시스템이나 Tailwind CSS, Ant Design, Material UI, Mantine, Chakra UI를 사용하면서도 `@refinedev/core`의 장점을 그대로 활용할 수 있습니다.

## Resource

**resource**는 `products`, `blogPosts`, `orders`처럼 애플리케이션의 엔터티를 나타냅니다. resource 정의는 라우트, CRUD 작업, 메뉴, providers를 하나의 구조로 연결해 줍니다.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        show: "/products/:id",
        edit: "/products/:id/edit",
        create: "/products/new",
      },
    ]}
  />
);
```

## Providers

providers는 데이터, 인증, 인가, 알림, i18n, 실시간, routing, 감사 추적 같은 주요 영역을 담당합니다. 기본 제공 provider를 쓰거나 직접 구현한 provider를 연결할 수 있습니다.

## Hooks

Refine의 hooks는 headless이고 라이브러리에 종속되지 않습니다. `useGo`, `useCan`, `useTranslate` 같은 API를 통해 이동, 권한, 번역을 일관된 방식으로 다룰 수 있습니다.

## Meta

`meta` 속성을 사용하면 providers와 hooks에 추가 정보를 전달할 수 있습니다. headers, 특수 파라미터, 필드 선택, multi-tenancy, GraphQL 쿼리 힌트 등에 유용합니다.
