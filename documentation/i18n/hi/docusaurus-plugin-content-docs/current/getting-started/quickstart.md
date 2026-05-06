---
title: "Quick Start | Refine v5 के साथ शुरुआत"
display_title: "Quick Start Guide"
sidebar_label: "Quick Start Guide"
description: "Browser scaffolder या CLI के साथ Refine v5 project शुरू करें और tutorial तक आगे बढ़ें।"
displayed_sidebar: mainSidebar
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import { Playground } from "@site/src/components/playground";

**Refine** किसी भी ऐसे environment में काम करता है जहाँ **React** चल सकता है, जैसे Vite, Next.js, Remix और CRA.

पैकेज manually install किए जा सकते हैं, लेकिन शुरुआत के लिए सबसे अच्छा तरीका browser-based scaffolder या CLI-based scaffolder है। दोनों विकल्प framework, UI integration, data provider, authentication और i18n चुनने की सुविधा देते हैं।

## CLI का उपयोग

नई **Refine** app जल्दी शुरू करने के लिए `create-refine-app` चलाएँ:

```sh
npm create refine-app@latest
```

CLI के prompts पूरे करें, बनी हुई directory में जाएँ, ज़रूरत पड़ने पर dependencies install करें और CLI द्वारा सुझाया गया dev server command चलाएँ।

## Browser का उपयोग

Browser scaffolder वही मुख्य विकल्प देता है जो CLI देता है, और download से पहले preview भी दिखाता है।

<Playground />

## आगे क्या करें

[Tutorials](/core/tutorial) देखें, [real-life examples](/core/templates) खोलें, या [General Concepts](/core/docs/guides-concepts/general-concepts/) और [Data Fetching](/core/docs/guides-concepts/data-fetching/) guides से सीखना शुरू करें।
