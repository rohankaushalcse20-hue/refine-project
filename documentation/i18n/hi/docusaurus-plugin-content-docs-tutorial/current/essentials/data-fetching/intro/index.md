---
title: Data Fetching
---

import { Sandpack, FocusOnDataProviderFile, AddDataProviderToRefine } from "./sandpack.tsx";

<Sandpack>

इस चरण में हम Refine में data fetching की बुनियादी बातें सीखेंगे। `<Refine />` component [`dataProvider`](/core/docs/core/refine-component/#dataprovider-) prop स्वीकार करता है, जिसका उपयोग simple interface के साथ data fetching और mutation operations संभालने के लिए किया जाता है। Refine में कई data providers out of the box supported हैं, लेकिन इस tutorial के लिए हम अपना data provider बनाएंगे और उसे [fake REST API](https://api.fake-rest.refine.dev/) से connect करेंगे।

Supported data providers के बारे में अधिक जानने के लिए Data Fetching guide का [Supported Data Providers](/core/docs/guides-concepts/data-fetching/#supported-data-providers) section देखें।

## Data Provider बनाना

हम हर method को एक-एक करके implement करेंगे, ताकि सभी details ठीक से cover हों। API requests के लिए हम `fetch` का उपयोग करेंगे, लेकिन आप अपनी पसंद की कोई भी library चुन सकते हैं।

सबसे पहले, हम अपने project में `src/providers/data-provider.ts` file बनाएंगे। इसी file में वे सभी methods होंगे जिन्हें हमें अपने data provider के लिए implement करना है।

Empty data provider देखने के लिए दाईं ओर panel में <FocusOnDataProviderFile>`src/providers/data-provider.ts` देखें</FocusOnDataProviderFile>।

इसके बाद, हम `src/App.tsx` file में `dataProvider` prop के जरिए अपना data provider `<Refine />` component को pass करेंगे।

नीचे दी गई lines जोड़कर अपनी `src/App.tsx` file update करें:

```tsx
import { Refine, WelcomePage } from "@refinedev/core";

// highlight-next-line
import { dataProvider } from "./providers/data-provider";

export default function App(): JSX.Element {
  return (
    // highlight-next-line
    <Refine dataProvider={dataProvider}>
      <WelcomePage />
    </Refine>
  );
}
```

<AddDataProviderToRefine />

:::tip

Refine के साथ multiple data providers का उपयोग करना भी संभव है। इसके बारे में आप Data Fetching guide के [Multiple Data Providers](/core/docs/guides-concepts/data-fetching/#multiple-data-providers) section में अधिक सीख सकते हैं।

:::

अगले चरण में हम Refine के `useOne` hook से record fetch करना सीखेंगे और अपने data provider में `getOne` method implement करेंगे।

</Sandpack>
