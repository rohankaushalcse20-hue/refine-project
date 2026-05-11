---
title: "Tables गाइड | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "Refine में useTable, pagination, filtering और sorting patterns का Hindi परिचय।"
---

Data-intensive applications में tables records को पढ़ने, filter करने और manage करने का प्राथमिक तरीका होती हैं। Refine की table integration इन common behaviors को reusable बनाती है।

## useTable

`useTable` hook listing flows के लिए state और fetching logic को संभालता है। इसके नीचे `useList` का उपयोग होता है, लेकिन API shape table-focused रहती है।

यह hook sorting, filtering और pagination state को data provider तक pass करता है ताकि server-side या client-side behavior implement किया जा सके।

## UI library support

Refine कई popular table implementations के साथ integrate कर सकता है:

- TanStack Table
- Ant Design Table
- Material UI DataGrid
- Mantine और Chakra UI integrations

## Pagination

Pagination के लिए `currentPage`, `pageSize` और `mode` जैसे options उपयोग किए जाते हैं। `mode` यह तय करता है कि pagination server-side होगी, client-side होगी या बंद रहेगी।

## Filtering और sorting

`filters` और `sorters` state के जरिए complex queries बनाना संभव है। इन states को hook APIs के जरिए बदला जा सकता है और provider इनका उपयोग API requests तैयार करने में करता है।
