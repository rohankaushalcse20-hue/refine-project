---
title: "Authorization | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "Access control provider के माध्यम से actions, routes और components पर permissions नियंत्रित करें।"
---

Authorization तय करता है कि authenticated user क्या कर सकता है। Refine में इसे `accessControlProvider` के माध्यम से मॉडल किया जाता है, जिसे hooks, buttons, menus और pages में उपयोग किया जा सकता है।

## Access control provider

इसका मुख्य method `can` है। यह resource, action और ज़रूरत पड़ने पर अतिरिक्त context लेता है, फिर access का फैसला लौटाता है।

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

`useCan` UI को permissions के अनुसार adapt करने में मदद करता है, लेकिन अंतिम authorization check backend पर ही रहना चाहिए।
