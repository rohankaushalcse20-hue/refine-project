---
title: "Link component | Refine v5"
display_title: "<Link />"
sidebar_label: "<Link />"
description: "Refine v5 में routing-aware navigation के लिए <Link /> component का Hindi परिचय।"
source: packages/core/src/components/link/index.tsx
---

`<Link />` एक component है जिसका उपयोग application के अलग-अलग pages पर navigate करने के लिए किया जाता है।

यह अंदरूनी रूप से [`routerProvider.Link`](/core/docs/routing/router-provider/#link) का उपयोग करता है। यदि [`routerProvider`](/core/docs/routing/router-provider/) उपलब्ध नहीं है, तो यह [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) HTML element का उपयोग करेगा।

## Usage

```tsx
import { Link } from "@refinedev/core";

const MyComponent = () => {
  return (
    <>
      {/* simple usage, navigates to `/posts` */}
      <Link to="/posts">Posts</Link>
      {/* complex usage with more control, navigates to `/posts` with query filters */}
      <Link
        go={{
          query: {
            // `useTable` or `useDataGrid` automatically uses these filters to fetch data if `syncWithLocation` is true.
            filters: [
              {
                operator: "eq",
                value: "published",
                field: "status",
              },
            ],
          },
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

## Props

`<Link />` component [`routerProvider.Link`](/core/docs/routing/router-provider/#link) के सभी props और `<a>` HTML element के props स्वीकार करता है। इनके अलावा यह `go` और `to` props भी लेता है, जिनकी मदद से `<Refine />` में परिभाषित किसी specific `resource` तक navigate किया जा सकता है।

### go

जब `go` prop दिया जाता है, तो यह component URL बनाने के लिए [`useGo`](/core/docs/routing/hooks/use-go/) का उपयोग करता है। यह `useGo.go` द्वारा स्वीकार किए जाने वाले सभी props ले सकता है।

यह तब उपयोगी होता है जब आप किसी resource के specific action पर जाना चाहते हैं।

:::caution

- इस prop का उपयोग करने के लिए `routerProvider` जरूरी है।
- यदि `to` prop भी दिया गया है, तो `go` को ignore किया जाएगा।

:::

### to

जिस URL पर navigate करना है।

## Type support with generics

`<Link />` किसी भी routing library के साथ काम करता है क्योंकि यह अंदरूनी रूप से [`routerProvider.Link`](/core/docs/routing/router-provider/#link) का उपयोग करता है। लेकिन `@refinedev/core` से import करने पर यह आपकी चुनी हुई routing library के लिए full type support नहीं देता। इसे सक्षम करने के लिए generics का उपयोग किया जा सकता है।

```tsx
import type { LinkProps } from "react-router";
import { Link } from "@refinedev/core";

const MyComponent = () => {
  return (
    // Omit 'to' prop from LinkProps (required by react-router) since we use the 'go' prop
    <Link<Omit<LinkProps, "to">>
      // Props from "react-router"
      // highlight-start
      replace={true}
      unstable_viewTransition={true}
      preventScrollReset={true}
      // highlight-end
      // Props from "@refinedev/core"
      go={{
        to: {
          resource: "posts",
          action: "list",
        },
      }}
    >
      Posts
    </Link>
  );
};
```
