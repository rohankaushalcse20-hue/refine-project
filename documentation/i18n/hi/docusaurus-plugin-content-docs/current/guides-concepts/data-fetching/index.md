---
title: "Data Fetching गाइड | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "Refine में data provider, data hooks, caching और multi-provider patterns का संक्षिप्त परिचय।"
---

Refine applications में data layer का केंद्र **data provider** होता है। यह [`DataProvider`](/core/docs/core/interface-references#dataprovider) interface लागू करता है और API से बात करके data को app तक पहुंचाता है।

Refine resource name, `id` और अन्य parameters आपके data provider तक pass करता है ताकि सही endpoints पर request भेजी जा सके।

## Data hooks

एक बार `dataProvider` दे देने के बाद आप `useOne`, `useList`, `useCreate`, `useUpdate` और `useDelete` जैसे hooks का उपयोग कर सकते हैं।

- `useOne` किसी एक record को fetch करने के लिए
- `useList` paginated collections के लिए
- `useUpdate` और दूसरे mutation hooks records बदलने के लिए

## State और caching

Refine data hooks के नीचे [TanStack Query](https://tanstack.com/query) का उपयोग करता है। इससे loading state, error state, cache invalidation और deduplicated requests जैसी सुविधाएं मिलती हैं।

## Multiple data providers

जरूरत पड़ने पर अलग-अलग resources के लिए अलग providers उपयोग किए जा सकते हैं। उदाहरण के लिए `posts` के लिए REST और `users` के लिए GraphQL।

## Meta usage

`meta` property के जरिए extra headers, tenant identifiers, custom parameters या GraphQL query metadata provider तक पहुंचाया जा सकता है।

```tsx
useOne({
  resource: "products",
  id: 1,
  meta: {
    foo: "bar",
  },
});
```

इसका exact behavior आपके data provider implementation पर निर्भर करता है।
