---
title: "Tables और Lists | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "Refine के साथ tables, lists, filters, sorting और pagination बनाएँ।"
---

Tables और lists API data को उपयोगी interface में बदलते हैं। Refine ऐसे hooks देता है जो pagination, filters, sorting और loading state को data provider से जोड़ते हैं।

## Lists

`useTable` और `useList` UI integrations या custom components के साथ list views बनाने के लिए आधारभूत hooks हैं।

```tsx
const table = useTable({
  resource: "products",
  pagination: { pageSize: 10 },
});
```

## Filters और sorting

Filters और sorters को ऐसे parameters में बदला जाता है जिन्हें data provider API तक भेजता है। इससे backend communication UI layer से अलग रहता है।

## CRUD actions

Lists को create, edit, show और delete actions से जोड़ा जा सकता है। इन actions में permissions और i18n labels दोनों शामिल किए जा सकते हैं।
