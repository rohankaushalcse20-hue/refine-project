---
title: "Data Fetching | Refine v5"
display_title: "Data Fetching"
sidebar_label: "Data Fetching"
description: "जानें कि Refine data providers और hooks के माध्यम से UI को API से कैसे जोड़ता है।"
---

Data किसी भी admin application का केंद्र होता है। Refine UI को एक या कई data sources से `dataProvider` के ज़रिए जोड़ता है, जो [`DataProvider`](/core/docs/core/interface-references#dataprovider) interface लागू करता है।

Data provider को `resource`, `id` और `meta` जैसी जानकारी मिलती है, और वही आपके API के सही endpoint से बात करता है।

## Data hooks

Provider register करने के बाद आप `useList`, `useOne`, `useCreate`, `useUpdate` और `useDelete` जैसे hooks से CRUD operations संभाल सकते हैं।

```tsx
import { useOne } from "@refinedev/core";

const Product = () => {
  const { data, isLoading } = useOne({ resource: "products", id: 1 });
  if (isLoading) return <span>Loading...</span>;
  return <pre>{JSON.stringify(data, null, 2)}</pre>;
};
```

## State और cache

Data hooks loading, error, success state, cache, request deduplication, invalidation और optimistic updates के लिए TanStack Query का उपयोग करते हैं।

## Multiple providers

आप एक resource के लिए REST और दूसरे resource के लिए GraphQL उपयोग कर सकते हैं, जबकि components के लिए API एक जैसा बना रहता है।
