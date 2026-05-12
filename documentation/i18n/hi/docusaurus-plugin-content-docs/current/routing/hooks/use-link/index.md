---
title: "useLink Hook | Refine v5"
display_title: "useLink"
sidebar_label: "useLink"
description: "Refine v5 में routing-aware Link component प्राप्त करने के लिए useLink hook का Hindi परिचय।"
---

`useLink` एक hook है जो [`<Link />`](/core/docs/routing/components/link/) component लौटाता है। इसका उपयोग application के अलग-अलग pages पर navigate करने के लिए किया जाता है।

:::simple Good to know

- सामान्य उपयोग के लिए `@refinedev/core` package से सीधे `<Link />` component का उपयोग करना बेहतर है। यह hook मुख्य रूप से internal purposes और customization scenarios के लिए expose किया गया है।

:::

## Usage

```tsx
import { useLink } from "@refinedev/core";

const MyComponent = () => {
  const Link = useLink();

  return (
    <>
      <Link to="/posts">Posts</Link>
      {/* or */}
      <Link
        go={{
          to: {
            resource: "posts",
            action: "list",
          },
        }}
      >
        Posts
      </Link>
    </>
  );
};
```
