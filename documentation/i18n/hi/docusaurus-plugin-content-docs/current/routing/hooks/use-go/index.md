---
title: "useGo Hook | Refine v5"
display_title: "useGo"
sidebar_label: "useGo"
description: "Refine v5 में path, resource object, query और hash के साथ navigation करने के लिए useGo hook का Hindi परिचय।"
---

`useGo` एक hook है जो navigation operations perform करने के लिए [`routerProvider`][routerprovider] के `go` method का उपयोग करता है।

## Usage

### Path के साथ

```tsx
import { useGo } from "@refinedev/core";

const MyComponent = () => {
  const go = useGo();

  return (
    <Button
      onClick={() => {
        go({
          to: "/posts",
          query: {
            filters: [
              {
                field: "title",
                operator: "contains",
                value: "Refine",
              },
            ],
          },
          type: "push",
        });
      }}
    >
      Go Posts With Default Filters
    </Button>
  );
};
```

### Resource के साथ

किसी resource पर navigate करने के लिए `to` नीचे दिए गए shape वाला object स्वीकार करता है:

```tsx
type ToWithResource = {
  resource: string; // resource name or identifier
  id?: BaseKey; // required when `action` is `"edit"`, `"show"`, or `"clone"`.
  action: "list" | "create" | "edit" | "show" | "clone"; // action name
  meta?: Record<string, unknown>; // meta data to be used when composing the path (use if you have additional path parameters)
};
```

`useGo`, resource object को `<Refine />` component के `resources` array में defined path में convert करेगा।

```tsx
import { useGo } from "@refinedev/core";

const MyComponent = () => {
    const go = useGo();

    return (
        <Button
            onClick={() => {
                go({
                    to:  {
                        resource: "posts", // resource name or identifier
                        action: "edit",
                        id: "1",
                    }
                    query: {
                         foo: "bar",
                    },
                    type: "push",
                });
            }}
        >
            Go Posts With Default Filters
        </Button>
    );
};
```

## Parameters

### to

`to` parameter वह path है जिस पर आप navigate करना चाहते हैं। खाली छोड़ने पर यह current path पर navigate करेगा, जो query parameters update करने के लिए उपयोगी है।

आप `to` parameter में `resource` object भी pass कर सकते हैं। `routerProvider` resource object को path में convert करेगा।

### query

`query` parameter वे query parameters हैं जिन्हें आप path में जोड़ना चाहते हैं। यह एक object है जिसे `routerProvider` query string में convert करेगा।

### type

`type` parameter navigation का प्रकार तय करता है। यह इनमें से एक हो सकता है:

- `push`: history stack में नई entry जोड़ता है।
- `replace`: history stack की current entry को replace करता है।
- `path`: दिए गए config के लिए navigation path लौटाता है। यह history stack mutate नहीं करता।

### hash

`hash` parameter वह hash है जिसे आप path में जोड़ना चाहते हैं।

### options.keepQuery

`options.keepQuery` boolean तय करता है कि current query parameters रखे जाएं या नहीं। `true` होने पर current query parameters नए query parameters के साथ merge होंगे। `false` होने पर current query parameters ignore किए जाएंगे।

### options.keepHash

`options.keepHash` boolean तय करता है कि current hash URL में रखा जाए या नहीं। `true` होने पर current hash URL में रहेगा। `false` होने पर current hash ignore किया जाएगा।

## Return Value

`useGo`, `path` type को छोड़कर कोई value return नहीं करता। `path` type दिए गए config के लिए navigation path लौटाता है और history stack mutate नहीं करता।

[routerprovider]: /core/docs/routing/router-provider
[basekey]: /core/docs/core/interface-references#basekey
