---
title: "useGetToPath Hook | Refine v5"
display_title: "useGetToPath"
sidebar_label: "useGetToPath"
description: "Refine v5 में resource और action से URL compose करने के लिए useGetToPath hook का Hindi परिचय।"
---

`useGetToPath` एक hook है जो दिए गए `resource` और `action` के लिए URL compose करने वाला function लौटाता है। यदि URL parameters और `meta` property उपलब्ध हों, तो यह उन्हें भी path बनाते समय उपयोग करता है।

यह तब उपयोगी होता है जब आपको किसी resource के specific action पर navigate करना हो और path अपने आप resource definition के अनुसार बनना चाहिए।

## Usage

```tsx
import { useGetToPath, useGo } from "@refinedev/core";

// Let's assume that we have a resource named `posts` and the `edit` action path is `/:authorId/posts/:id/edit`

const MyComponent = () => {
  const getToPath = useGetToPath();

  const go = useGo();

  return (
    <Button
      onClick={() => {
        go({
          to: getToPath({
            resource: {
              name: "posts",
            },
            action: "edit",
            meta: {
              id: 1,
              authorId: 2,
            },
          }),
        });
      }}
    >
      Go To Edit Post
    </Button>
  );

  /* ... */
};
```

:::tip

यदि `authorId` और `id` parameters URL में मौजूद हैं, तो वे route से infer किए जाएंगे। यदि किसी parameter की value स्पष्ट रूप से set करनी हो, तो `meta` property का उपयोग करें।

:::

## Parameters

### resource

वह resource name जिसे आप navigate करना चाहते हैं।

### action

वह action name जिसे आप navigate करना चाहते हैं।

### meta

URL compose करते समय उपयोग होने वाला meta object। इसे URL से parse किए गए `params` object के साथ merge किया जाता है।
