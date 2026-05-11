---
title: "Routing | Refine v5"
display_title: "라우팅"
sidebar_label: "라우팅"
description: "React Router, Next.js, Remix와 함께 Refine의 routing을 구성하는 방법을 설명합니다."
---

routing은 CRUD 애플리케이션의 중심입니다. Refine의 headless 아키텍처 덕분에 특정 framework에 묶이지 않고 원하는 라우터를 선택할 수 있습니다.

Refine는 **React Router**, **Next.js**, **Remix**용 통합을 제공하며 다음과 같은 이점이 있습니다.

- hooks와 components에서 파라미터를 자동으로 감지할 수 있음
- mutation이나 인증 상태 변경 후 자동 리다이렉션 가능
- navigation, breadcrumbs, 메뉴 생성을 위한 유틸리티 제공

Refine는 router-agnostic이므로 실제 라우트 정의는 여전히 애플리케이션에서 직접 관리합니다. React Router는 `Routes`, Next.js는 `pages` 또는 `app`, Remix는 `app/routes` 디렉터리를 사용합니다.

## Router provider 통합하기

원하는 통합 패키지를 import한 뒤 `<Refine />`의 `routerProvider`에 전달합니다.

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Routes } from "react-router";

export const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* Your route definitions */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

## 권장 사항

routes와 resources의 대응 관계를 맞추고, 명명 규칙을 일관되게 유지하고, 가능하면 `resource`나 `id` 같은 파라미터는 router에서 hooks로 자연스럽게 전달되도록 구성하세요.
