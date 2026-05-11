---
title: "Authorization गाइड | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "Refine में access control provider, useCan और CanAccess component की Hindi summary।"
---

Authorization यह तय करता है कि user किसी resource को देख सकता है या किसी action को चला सकता है या नहीं। Refine यह काम **Access Control Provider** के जरिए करता है।

Refine RBAC, ABAC, ACL या किसी भी custom authorization strategy के साथ काम कर सकता है, बशर्ते आप provider को सही decision logic दें।

## Access Control Provider

Access control setup का मुख्य entry point `can` method है। Refine resource, action और params देकर पूछता है कि access दिया जाना चाहिए या नहीं।

```tsx title="access-control-provider.ts"
import { AccessControlProvider } from "@refinedev/core";

export const accessControlProvider: AccessControlProvider = {
  can: async ({ resource, action, params }) => {
    if (meetSomeCondition) {
      return { can: true };
    }

    return {
      can: false,
      reason: "Unauthorized",
    };
  },
};
```

## CanAccess component

`CanAccess` component unauthorized users से pages या UI sections छिपाने के लिए उपयोगी है। यह internally provider के `can` method को call करता है।

## useCan hook

`useCan` hook imperatively access checks चलाने के लिए उपयोगी है। इसका उपयोग buttons, menu items, inline actions या custom views में किया जा सकता है।

## UI integrations

Refine की UI integrations access control results के आधार पर buttons, menu items और actions को hide या disable करने में मदद करती हैं। इससे UX और security दोनों consistent रहते हैं।
