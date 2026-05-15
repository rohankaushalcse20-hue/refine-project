---
title: Devtools का उपयोग
---

import { Sandpack, SelectorButtonIcon } from "./sandpack.tsx";

<Sandpack>

इस step में हम Refine के powerful Devtools package को explore करेंगे, जो Refine applications inspect और debug करने के लिए monitoring और update features देता है।

:::note

`@refinedev/devtools` beta stage में है और जल्द ही और features तथा improvements के साथ update होगा।

:::

`@refinedev/devtools` package development process में मदद करने के लिए बनाया गया है और production builds से हटा दिया जाएगा। आपकी application पर कोई performance impact नहीं होगा और production bundle में कोई leftover code नहीं रहेगा।

## Installation

Package installation straightforward है, लेकिन `@refinedev/cli` package Devtools package install और setup करने के लिए command भी देता है। Devtools package install करने के लिए हम नीचे दिया command उपयोग करेंगे:

<Tabs>

<TabItem value="cli" label="Using CLI" default>

```sh
npm run refine devtools init
```

</TabItem>

<TabItem value="manual" label="manual">

<InstallPackagesCommand args="@refinedev/devtools" />

फिर हमें अपनी application को `<DevtoolsProvider />` component से wrap करना होगा। `<DevtoolsProvider />` component को `App` component में `<Refine />` component के around wrap किया जाना चाहिए। Application में Devtools खोलने के लिए एक आसान shortcut पाने के लिए हम `<DevtoolsPanel />` component भी import करेंगे।

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";
// highlight-next-line
import { DevtoolsProvider, DevtoolsPanel } from "@refinedev/devtools";
/* ... */

export default function App() {
    return (
        {/* highlight-start */}
        {/* You can mount the DevtoolsProvider at the top most level of the element tree */}
        <DevtoolsProvider>
        {/* highlight-end */}
            <Refine>
                {/* ... */}
            </Refine>
            {/* highlight-start */}
            {/* DevtoolsPanel component should be mounted inside the DevtoolsProvider */}
            <DevtoolsPanel />
            {/* highlight-end */}
            {/* ... */}
        {/* highlight-next-line */}
        </DevtoolsProvider>
    );
}
```

इसके बाद हम अपनी application में Devtools का उपयोग शुरू कर सकते हैं।

</TabItem>

</Tabs>

## Monitoring Feature का उपयोग

Devtools package install और setup करने के बाद application के bottom पर एक छोटा devtools panel दिखेगा। Panel पर click करने से devtools खुलेंगे। फिर sidebar में `"Monitor"` पर click करके monitoring screen खोल सकते हैं।

इस screen में currentPage session के दौरान आपकी application में trigger हुई सभी queries और mutations शामिल होंगी। आप response, target data provider, target resource, query/mutation execute होने में लगा समय, और बहुत सारी details देख सकते हैं।

आप queries और mutations को उनके type, resource, status, और उन्हें trigger करने वाले component/hook के आधार पर filter कर पाएंगे। साथ ही, selector का उपयोग करके अपनी UI पर वह component चुन सकते हैं जिसके आधार पर filter करना है।

Selector उपयोग करने के लिए <SelectorButtonIcon /> icon पर click करें। जब आप page पर किसी ऐसे component पर hover करेंगे जिसने query या mutation trigger की है, तो component के around highlight दिखेगा। Component पर click करने से queries और mutations उसी component के आधार पर filter होंगी।

<VideoInView src="https://refine.ams3.cdn.digitaloceanspaces.com/assets/tutorial/webm/devtools-xray-3.webm" playsInline loop autoPlay muted />

## Update Feature का उपयोग

Devtools package की update feature `@refinedev/cli` के update command जैसी है और single click में Refine dependencies update करने के लिए एक उपयोगी UI देती है। इसी panel से आप single click में अपनी application में नए Refine packages भी add कर सकते हैं और उनका उपयोग करना सीख सकते हैं।

Available updates देखने के लिए `"Overview"` tab देखें और अपनी application में नए Refine packages add करने के लिए `"Add Package"` button पर click करें।

</Sandpack>
