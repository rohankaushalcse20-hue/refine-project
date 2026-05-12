---
title: "useBack Hook | Refine v5"
display_title: "useBack"
sidebar_label: "useBack"
description: "Refine v5 में history stack में वापस जाने के लिए useBack hook का Hindi परिचय।"
---

`useBack` एक hook है जो [`routerProvider`][routerprovider] के `back` method का उपयोग करके history stack में "go back" operation चलाता है।

## Usage

```tsx
import { useBack } from "@refinedev/core";

const MyComponent = () => {
  const back = useBack();

  return <Button onClick={() => back()}>Go Back</Button>;
};
```

[routerprovider]: /core/docs/routing/router-provider
