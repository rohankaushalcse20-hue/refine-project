---
title: "인가 | Refine v5"
display_title: "인가"
sidebar_label: "인가"
description: "access control provider를 이용해 actions, routes, components 접근 권한을 제어합니다."
---

인가는 인증된 사용자가 무엇을 할 수 있는지 정의합니다. Refine에서는 `accessControlProvider`를 사용해 hooks, buttons, menus, pages에서 권한을 조회할 수 있습니다.

## Access control provider

핵심 메서드는 `can`입니다. `resource`, `action`, 추가 파라미터를 받아 해당 작업을 허용할지 결정합니다.

```tsx
const accessControlProvider = {
  can: async ({ resource, action }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Only admins can delete posts" };
    }

    return { can: true };
  },
};
```

## Components에서 사용하기

`useCan`을 사용하면 권한에 따라 UI를 분기할 수 있습니다.

```tsx
const { data } = useCan({ resource: "posts", action: "delete" });

return data?.can ? <DeleteButton /> : null;
```

## 권장 사항

access control provider는 UI 경험을 개선하는 데 유용하지만, 최종 검증은 반드시 backend에서도 수행해야 합니다.
