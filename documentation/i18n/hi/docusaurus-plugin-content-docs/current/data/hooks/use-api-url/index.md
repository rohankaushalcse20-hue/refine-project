---
title: "useApiUrl Hook | Refine v5"
display_title: "useApiUrl"
sidebar_label: "useApiUrl"
description: "Refine v5 में current या named data provider का API URL प्राप्त करने के लिए useApiUrl hook का Hindi परिचय।"
source: packages/core/src/data/hooks/useApiUrl.ts
---

`useApiUrl` एक React hook है जो API URL लौटाता है। यह [`dataProvider`][data provider] से API URL प्राप्त करने के लिए `getApiUrl` method का उपयोग करता है।

यह तब उपयोगी होता है जब आपको अपने custom hooks या custom requests में API URL चाहिए।

## Usage

`useApiUrl` hook current resource के `dataProvider` से `getApiUrl` method call करेगा और उसका result लौटाएगा। यदि कोई resource infer नहीं हो पाता, तो यह default data provider का URL लौटाता है।

```tsx
//highlight-next-line
import { useCustom, useApiUrl } from "@refinedev/core";

interface PostUniqueCheckResponse {
  isAvailable: boolean;
}

//highlight-next-line
const apiUrl = useApiUrl();

const { data, isLoading } = useCustom<PostUniqueCheckResponse>({
  //highlight-next-line
  url: `${apiUrl}/posts-unique-check`,
  method: "get",
  config: {
    query: {
      title: "Foo bar",
    },
  },
});
```

`useApiUrl` hook optional `dataProviderName` parameter भी स्वीकार करता है। इससे आप current resource की परवाह किए बिना किसी खास `dataProvider` का URL प्राप्त कर सकते हैं।

```tsx
export const App: React.FC = () => {
    return (
        <Refine
            // highlight-start
            dataProvider={{
                default: dataProvider("https://api.fake-rest.refine.dev/"),
                other: dataProvider("https://other-api.fake-rest.refine.dev/"),
            }}
            // highlight-end
        >
            {/* ... */}
        </Refine>
    );
};
    ...
</Refine>


const apiUrl = useApiUrl("other");
//    ^ https://other-api.fake-rest.refine.dev/
```

## API Reference

### Return value

| Description | Type     |
| ----------- | -------- |
| API URL     | `string` |

[data provider]: /core/docs/data/data-provider
