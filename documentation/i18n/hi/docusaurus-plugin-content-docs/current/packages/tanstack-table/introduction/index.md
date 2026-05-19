---
title: "TanStack Table Introduction | Refine v5"
display_title: "Introduction"
sidebar_label: "Introduction"
description: "Refine v5 में @refinedev/react-table और TanStack Table integration शुरू करने के लिए Hindi introduction।"
source: /packages/react-table/src/useTable
---

import BaseHeadlessTable from "../examples/headless";
import BaseMantineTable from "../examples/mantine";
import BaseChakraUiTable from "../examples/chakra-ui";

# TanStack Table <GuideBadge id="guides-concepts/tables" /> <RouterBadge id="guides-concepts/routing/#usetable" />

Refine, [TanStack Table][tanstack-table] library के लिए integration package देता है। यह package tables को headless तरीके से manage करने देता है। यह adapter [TanStack Table][tanstack-table] और [Refine के useTable][use-table-core] hook, दोनों की features (sorting, filtering, pagination आदि) support करता है। सरल शब्दों में, आप [TanStack Table][tanstack-table] examples को अपने project में copy-paste करके as-is उपयोग कर सकते हैं।

## Installation

[`@refinedev/react-table`][refine-react-table] library install करें।

<InstallPackagesCommand args="@refinedev/react-table"/>

## Usage

आइए देखें कि [useTable][use-table-tanstack] hook के साथ table कैसे दिखाते हैं।

हम Mantine और Chakra UI के लिए implementation examples देते हैं। यदि आप कोई अलग UI library उपयोग कर रहे हैं, तो headless example को starting point की तरह उपयोग कर सकते हैं।

<Tabs wrapContent={false}>

<TabItem value="headless" label="Headless">

<BaseHeadlessTable />

</TabItem>

<TabItem value="mantine" label={(<span><span className="block">Mantine</span><small className="block">TanStack Table</small></span>)}>

<BaseMantineTable />

</TabItem>

<TabItem value="chakra-ui" label={(<span><span className="block">Chakra UI</span><small className="block">TanStack Table</small></span>)}>

<BaseChakraUiTable />

</TabItem>

</Tabs>

[tanstack-table]: https://tanstack.com/table/v8
[refine-react-table]: https://github.com/refinedev/refine/tree/main/packages/react-table
[use-table-core]: /core/docs/data/hooks/use-table
[use-table-tanstack]: /core/docs/packages/list-of-packages
[baserecord]: /core/docs/core/interface-references#baserecord
[httperror]: /core/docs/core/interface-references#httperror
[syncwithlocationparams]: /core/docs/core/interface-references#syncwithlocationparams
[notification-provider]: /core/docs/notification/notification-provider
[crudsorting]: /core/docs/core/interface-references#crudsorting
[crudfilters]: /core/docs/core/interface-references#crudfilters
[Refine swl]: /core/docs/core/refine-component#syncwithlocation
