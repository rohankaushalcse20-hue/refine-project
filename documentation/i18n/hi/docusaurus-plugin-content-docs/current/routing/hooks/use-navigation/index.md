---
title: "useNavigation Hook | Refine v5"
display_title: "useNavigation"
sidebar_label: "useNavigation"
description: "Refine v5 में legacy navigation helpers और URL builders समझने के लिए useNavigation hook का Hindi परिचय।"
---

`useNavigation` एक hook है जो app में navigate करने के methods देता है। Internally यह [`routerProvider`][routerprovider] के `go` method का उपयोग करता है।

यह hook legacy है और deprecated न होने के बावजूद recommended नहीं है। Custom navigation संभालते समय अपने router library के hooks और methods का उपयोग करना बेहतर है।

यदि आपको actions और resources के बीच navigate करने के लिए navigation hook चाहिए, तो हम [`useGo`](/core/docs/routing/hooks/use-go/) और [`useGetToPath`](/core/docs/routing/hooks/use-get-to-path/) hooks उपयोग करने की सलाह देते हैं।

```tsx
import { useNavigation } from "@refinedev/core";

const {
  list,
  create,
  edit,
  show,
  clone,
  listUrl,
  createUrl,
  editUrl,
  showUrl,
  cloneUrl,
} = useNavigation();
```

## Return Values

`useNavigation` hook द्वारा लौटाए गए सभी functions `meta` parameter स्वीकार करते हैं। यह optional parameter है, जिसका उपयोग routes में `id` के अलावा additional parameters होने पर उन्हें pass करने के लिए किया जा सकता है।

### list

यह method दिए गए resource के list page पर navigate करता है।

```tsx
import { useNavigation } from "@refinedev/core";

const { list } = useNavigation();

list("posts"); // It navigates to the `/posts` page
```

आप `list` method में second parameter के रूप में `type` property भी दे सकते हैं।

### create

यह method दिए गए resource के create page पर navigate करता है।

```tsx
import { useNavigation } from "@refinedev/core";

const { create } = useNavigation();

create("posts"); // It navigates to the `/posts/create` page
```

आप `create` method में second parameter के रूप में `type` property भी दे सकते हैं।

### edit

यह method दिए गए `resource` और `id` के edit page पर navigate करता है। इस method का उपयोग करते समय आपको उस record का `id` देना होगा जिसे edit करना है।

```tsx
import { useNavigation } from "@refinedev/core";

const { edit } = useNavigation();

edit("posts", "1"); // It navigates to the `/posts/edit/1` page
```

आप `edit` method में third parameter के रूप में `type` property भी दे सकते हैं।

### show

यह method दिए गए `resource` और `id` के show page पर navigate करता है। इस method का उपयोग करते समय आपको उस record का `id` देना होगा जिसे show करना है।

```tsx
import { useNavigation } from "@refinedev/core";

const { show } = useNavigation();

show("posts", "1"); // It navigates to the `/posts/show/1` page
```

आप `show` method में third parameter के रूप में `type` property भी दे सकते हैं।

### clone

यह method दिए गए `resource` और `id` के clone page पर navigate करता है। इस method का उपयोग करते समय आपको उस record का `id` देना होगा जिसे clone करना है।

```tsx
import { useNavigation } from "@refinedev/core";

const { clone } = useNavigation();

clone("posts", "1"); // It navigates to the `/posts/clone/1` page
```

आप `clone` method में third parameter के रूप में `type` property भी दे सकते हैं।

### listUrl

यह method दिए गए resource का list page URL लौटाता है।

```tsx
import { useNavigation } from "@refinedev/core";

const { listUrl } = useNavigation();

listUrl("posts"); // It returns the `/posts` URL
```

### createUrl

यह method दिए गए resource का create page URL लौटाता है।

```tsx
import { useNavigation } from "@refinedev/core";

const { createUrl } = useNavigation();

createUrl("posts"); // It returns the `/posts/create` URL
```

### editUrl

यह method दिए गए resource और id का edit page URL लौटाता है।

```tsx
import { useNavigation } from "@refinedev/core";

const { editUrl } = useNavigation();

editUrl("posts", "1"); // It returns the `/posts/edit/1` URL
```

### showUrl

यह method दिए गए resource और id का show page URL लौटाता है।

```tsx
import { useNavigation } from "@refinedev/core";

const { showUrl } = useNavigation();

showUrl("posts", "1"); // It returns the `/posts/show/1` URL
```

### cloneUrl

यह method दिए गए resource और id का clone page URL लौटाता है।

```tsx
import { useNavigation } from "@refinedev/core";

const { cloneUrl } = useNavigation();

cloneUrl("posts", "1"); // It returns the `/posts/clone/1` URL
```

## API Reference

### Return values

| Property  | Description                              | Type                                                                                     |
| --------- | ---------------------------------------- | ---------------------------------------------------------------------------------------- |
| list      | Method that navigates to the list page   | `(resource: string, type: HistoryType, meta?: Record<string, any>) => void`              |
| create    | Method that navigates to the create page | `(resource: string, type: HistoryType, meta?: Record<string, any>) => void`              |
| edit      | Method that navigates to the edit page   | `(resource: string, id: BaseKey, type: HistoryType, meta?: Record<string, any>) => void` |
| show      | Method that navigates to the show page   | `(resource: string, id: BaseKey, type: HistoryType, meta?: Record<string, any>) => void` |
| clone     | Method that navigates to the clone page  | `(resource: string, id: BaseKey, type: HistoryType, meta?: Record<string, any>) => void` |
| listUrl   | Method that returns the list page URL    | `(resource: string, meta?: Record<string, any>) => string`                               |
| createUrl | Method that returns the create page URL  | `(resource: string, meta?: Record<string, any>) => string`                               |
| editUrl   | Method that returns the edit page URL    | `(resource: string, id: BaseKey, meta?: Record<string, any>) => string`                  |
| showUrl   | Method that returns the show page URL    | `(resource: string, id: BaseKey, meta?: Record<string, any>) => string`                  |
| cloneUrl  | Method that returns the clone page URL   | `(resource: string, id: BaseKey, meta?: Record<string, any>) => string`                  |

#### Interfaces

- [`type BaseKey`][basekey]
- `type HistoryType = "push" | "replace";`

[routerprovider]: /core/docs/routing/router-provider
[basekey]: /core/docs/core/interface-references#basekey
