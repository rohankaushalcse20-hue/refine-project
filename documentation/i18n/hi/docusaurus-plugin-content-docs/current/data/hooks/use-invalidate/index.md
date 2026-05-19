---
title: "useInvalidate Hook | Refine v5"
display_title: "useInvalidate"
sidebar_label: "useInvalidate"
description: "Refine v5 में resource या dataProvider query state invalidate करने के लिए useInvalidate hook का Hindi परिचय।"
source: /packages/core/src/hooks/invalidate
---

`useInvalidate` एक hook है जिसका उपयोग किसी specific `resource` या [`dataProvider`][data-provider] (dataProviderName के साथ) की state invalidate करने के लिए किया जा सकता है।

Mutation hook successful होने पर यह hook call किया जाता है। उदाहरण के लिए, [useCreate](/core/docs/data/hooks/use-create/) hook से `Posts` create करने पर `Posts` resource की `list` ([useList](/core/docs/data/hooks/use-list/)) और `many` ([useMany](/core/docs/data/hooks/use-many/)) state invalidate होगी।

:::simple Good to know

- यह hook Refine internally उपयोग करता है। अधिकतर cases में आपको इसकी जरूरत नहीं होगी, लेकिन custom invalidation की जरूरत वाले use cases के लिए इसे export किया गया है।
- Refine data fetch और state manage करने के लिए [TanStack Query](https://tanstack.com/query/latest) का उपयोग करता है। Invalidation के बारे में अधिक जानकारी के लिए TanStack Query की [invalidation](https://tanstack.com/query/v5/docs/react/guides/query-invalidation) docs पढ़ें।

:::

## Basic Usage

```ts
import { useInvalidate } from "@refinedev/core";

const invalidate = useInvalidate();

// `invalidate` function is async and returns a promise. If you want to wait for the invalidation process to complete, you can await it.
invalidate({
  resource: "posts",
  invalidates: ["list"],
});
```

## Examples

Posts `resource` की `"list"` और `"many"` states invalidate करने के लिए:

```ts
invalidate({
  resource: "posts",
  invalidates: ["list", "many"],
});
```

`1` id वाले Posts की state invalidate करने के लिए:

```ts
invalidate({
  resource: "posts",
  invalidates: ["detail"],
  id: 1,
});
```

`"second-data-provider"` नाम वाले [`dataProvider`][data-provider] के Posts `resource` की `"list"` और `"many"` states invalidate करने के लिए:

```ts
invalidate({
  resource: "posts",
  dataProviderName: "second-data-provider",
  invalidates: ["list"],
});
```

`"second-data-provider"` नाम वाले [`dataProvider`][data-provider] की सभी states invalidate करने के लिए:

```ts
invalidate({
  dataProviderName: "second-data-provider",
  invalidates: ["all"],
});
```

Posts की सभी states invalidate करने के लिए:

```ts
invalidate({
  resource: "posts",
  invalidates: ["resourceAll"],
});
```

## Invalidation Parameters

### resource

`resource` API endpoint में किसी entity को represent करता है (जैसे https://api.fake-rest.refine.dev/posts)। यह किसी specific resource की state invalidate करने के लिए उपयोग होता है।

### id

`"detail"` state invalidate करते समय उपयोग होने वाला `id`।

### dataProviderName

यदि एक से अधिक [`dataProvider`][data-provider] हैं, तो `dataProviderName` prop pass करके बताएं कि किस provider का उपयोग करना है।

### invalidates <PropTag required />

Invalidation process का scope। ये scopes array में दिए जा सकते हैं।

- `"all"`: सभी resources की सभी states invalidate करता है।
- `"resourceAll"`: दिए गए `resource` की सभी states invalidate करता है।
- `"list"`: दिए गए `resource` की `"list"` state invalidate करता है।
- `"detail"`: दिए गए `resource` और `id` की `"detail"` state invalidate करता है।
- `"many"`: दिए गए `resource` की `"many"` state invalidate करता है।

### invalidationFilters and invalidationOptions

Invalidation process में कौन-सी queries invalidate करनी हैं, यह चुनते समय लागू होने वाले filters और options। Default रूप से Refine invalidation process को fine-tune करने के लिए कुछ filters और options apply करता है।

Default settings में सभी targeted queries invalidate होती हैं और active queries refetch के लिए trigger होती हैं। यदि कोई ongoing queries हैं, तो उन्हें वैसे ही रखा जाता है।

## API Reference

### Invalidation Parameters

| Property                         | Description                                                       | Type                                                                                                                    | Default                                  |
| -------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| invalidated <PropTag asterisk /> | The states you want to invalidate.                                | `all`, `resourceAll`, `list`, `many`, `detail`, `false`                                                                 |                                          |
| resource                         | Resource name for State invalidation.                             | `string`                                                                                                                |                                          |
| id                               | The `id` to use when invalidating the "detail" state.             | [`BaseKey`](/core/docs/core/interface-references#basekey)                                                               |                                          |
| dataProviderName                 | The name of the data provider whose state you want to invalidate. | `string`                                                                                                                | `default`                                |
| invalidationFilters              | The filters to use when picking queries to invalidate             | [`InvalidateQueryFilters`](https://tanstack.com/query/v5/docs/react/reference/QueryClient#queryclientinvalidatequeries) | `{ type: "all", refetchType: "active" }` |
| invalidationOptions              | The options to use in the invalidation process                    | [`InvalidateOptions`](https://tanstack.com/query/v5/docs/react/reference/QueryClient#queryclientinvalidatequeries)      | `{ cancelRefetch: false }`               |

[data-provider]: /core/docs/data/data-provider
