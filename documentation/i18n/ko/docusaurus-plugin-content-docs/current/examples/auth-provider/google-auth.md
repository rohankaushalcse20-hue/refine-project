---
id: google-auth
title: "Google Auth 예제 | Refine v5 Auth Provider"
display_title: "Google Auth"
sidebar_label: "Google Auth"
description: "Refine v5에서 Google Auth 예제를 구성하는 방법을 살펴봅니다. 실제 React admin panel을 위한 provider pattern과 code snippet을 확인합니다."
example-tags: [auth-provider]
---

Google Login을 사용하면 애플리케이션의 접근을 제어하고 사용자 identity를 제공할 수 있습니다. 이 예제는 Refine를 사용해 프로젝트에 Google Login을 연결하는 방법을 안내합니다.

:::note

자체 OAuth application을 개발하는 경우, 배포된 애플리케이션 URL과 로컬 개발 URL을 모두 OAuth app settings의 allowed origins 목록에 추가하는 것이 중요합니다. 추가하지 않으면 앱이 실패할 수 있습니다.

더 자세한 안내는 이 [video tutorial](https://www.youtube.com/watch?v=HtJKUQXmtok)을 참고할 수 있습니다.

:::

<CodeSandboxExample path="auth-google-login" />
