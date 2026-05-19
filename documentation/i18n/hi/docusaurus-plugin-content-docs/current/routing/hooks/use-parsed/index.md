---
title: "useParsed Hook | Refine v5"
display_title: "useParsed"
sidebar_label: "useParsed"
description: "Refine v5 में current URL, query parameters और inferred resource/action/id पढ़ने के लिए useParsed hook का Hindi परिचय।"
---

`useParsed` एक hook है जो [`routerProvider`][routerprovider] के `parse` method का उपयोग करके URL और query parameters तक access देता है। यह URL से inferred `resource`, `action` और `id` भी लौटाता है।

## Usage

```tsx
import { useParsed } from "@refinedev/core";

type MyParams = {
  someParam: string;
};

const MyComponent = () => {
  const {
    resource,
    action,
    id,
    pathname,
    params: {
      filters,
      sorters,
      currentPage,
      pageSize,
      ...restParams // TParams - Any other parameters are also parsed and available in `params`
    },
  } = useParsed<MyParams>();

  /* ... */
};
```

## Return Values

### resource

यह active resource है, जो current route और `<Refine />` component के `resources` array में दिए गए action definitions से match होता है। यदि कोई match नहीं मिलता, तो यह `undefined` होगा।

### action

यह active action है, जो current route और `<Refine />` component के `resources` array में दिए गए action definitions से match होता है। यदि कोई match नहीं मिलता, तो यह `undefined` होगा।

### id

यह Refine के API interactions में उपयोग होने वाला मुख्य parameter है। यह `params` object में भी उपलब्ध रहता है, लेकिन convenience के लिए अलग value के रूप में भी लौटाया जाता है। URL में `id` parameter न होने पर यह `undefined` होगा।

### pathname

URL का current pathname।

### params.filters

URL से parse किए गए filters। यदि URL में `filters` parameter नहीं है, तो यह `undefined` होगा। यह property `useTable` की `syncWithLocation` feature में उपयोग होती है।

### params.sorters

URL से parse किए गए sorters। यदि URL में `sorters` parameter नहीं है, तो यह `undefined` होगा। यह property `useTable` की `syncWithLocation` feature में उपयोग होती है।

### params.currentPage

URL से parse किया गया current page। यदि URL में `currentPage` parameter नहीं है, तो यह `undefined` होगा। यह property `useTable` की `syncWithLocation` feature में उपयोग होती है।

### params.pageSize

URL से parse किया गया page size। यदि URL में `pageSize` parameter नहीं है, तो यह `undefined` होगा। यह property `useTable` की `syncWithLocation` feature में उपयोग होती है।

### params

यह object URL से parse किए गए सभी parameters रखता है। URL में कोई parameter न होने पर यह empty object होगा। `params` object में URL parameters और query parameters, दोनों शामिल होते हैं।

[routerprovider]: /core/docs/routing/router-provider
