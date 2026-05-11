---
title: "Quickstart | Refine v5 시작하기"
display_title: "빠른 시작 가이드"
sidebar_label: "빠른 시작 가이드"
description: "브라우저 scaffolder 또는 CLI를 사용해 Refine v5 프로젝트를 만들고 다음 학습 경로로 이동합니다."
displayed_sidebar: mainSidebar
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import { Playground } from "@site/src/components/playground";

**Refine**은 Vite, Next.js, Remix, CRA 등 **React**를 실행할 수 있는 환경이라면 어디서든 동작합니다.

패키지를 직접 추가해도 되지만, 가장 빠른 시작 방법은 브라우저 기반 scaffolder 또는 CLI를 사용하는 것입니다. 두 방식 모두 프로젝트 생성 전에 framework, UI, data provider, 인증, i18n 구성을 선택할 수 있습니다.

## CLI 사용하기

`create-refine-app`을 실행해 대화형으로 새 **Refine** 프로젝트를 생성합니다.

```sh
npm create refine-app@latest
```

질문에 답한 뒤 생성된 디렉터리로 이동하고, 필요하면 의존성을 설치한 다음 CLI가 안내하는 명령으로 개발 서버를 실행하세요.

## 브라우저 사용하기

브라우저 기반 scaffolder도 CLI와 같은 핵심 옵션을 제공합니다. 다운로드 전에 결과 화면을 미리 확인할 수 있다는 점도 장점입니다.

<Playground />

## 다음 단계

[Tutorial](/core/tutorial)로 이동해 초기 프로젝트를 완전한 CRUD 애플리케이션으로 발전시키거나, [실전 템플릿](/core/templates)을 살펴보고 [General Concepts](/core/docs/guides-concepts/general-concepts/)와 [Data Fetching](/core/docs/guides-concepts/data-fetching/) 가이드도 함께 읽어보세요.
