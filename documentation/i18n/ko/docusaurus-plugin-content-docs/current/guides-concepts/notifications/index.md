---
title: "알림 | Refine v5"
display_title: "알림"
sidebar_label: "알림"
description: "Refine의 notification provider로 성공 및 오류 메시지를 표시합니다."
---

알림은 작업 성공을 확인하거나 오류를 설명할 때 유용합니다. Refine는 `notificationProvider`를 통해 hooks, mutations, components에서 메시지를 표시합니다.

## Notification provider

provider는 일반적으로 메시지를 띄우는 `open` 메서드와 필요 시 닫는 `close` 메서드를 제공합니다.

```tsx
const notificationProvider = {
  open: ({ type, message, description }) => {
    console.log(type, message, description);
  },
  close: (key) => {
    console.log("close", key);
  },
};
```

## UI integrations

Ant Design, Material UI, Mantine, Chakra UI 통합을 사용하면 각 라이브러리의 알림 시스템을 Refine에 연결할 수 있습니다.

## i18n

로컬라이즈된 애플리케이션에서는 성공, 실패, 경고 메시지가 사용자의 언어로 자연스럽게 읽히도록 알림 제목과 설명도 함께 번역해야 합니다.
