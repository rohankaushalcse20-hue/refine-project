---
title: आपका पहला Refine app
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

नया Refine app बनाना बहुत आसान है और कुछ ही चरणों में एक पूरी तरह काम करने वाला app तैयार हो जाता है। इस tutorial के लिए हम `create-refine-app` की पूरी क्षमता का उपयोग नहीं करेंगे। इसके बजाय हम एक खाली app बनाएंगे, जरूरी dependencies install करेंगे और app को manually configure करेंगे।

<Tabs wrapContent={false}>

<TabItem value="quick" label="Quick Setup">

इस tutorial को साथ-साथ follow करने के लिए आप `create-refine-app` द्वारा दिए गए starter templates का उपयोग कर सकते हैं। नीचे दिया गया command आपके लिए `@refinedev/core` और `@refinedev/cli` packages के साथ एक नया empty project बनाएगा, जिसमें tutorial शुरू करने के लिए जरूरी सब कुछ होगा।

```sh
npm create refine-app@latest -- --example starter-vite
```

</TabItem>

<TabItem value="manual" label="Manual Setup">

हमें सही templates का उपयोग करके app बनाना होगा। उसके बाद हम Refine dependencies install करेंगे और app को configure करेंगे।

```sh
npm create vite@latest my-refine-app -- --template react-ts
```

Vite और project creation के बारे में अधिक जानने के लिए आप [Vite documentation](https://vitejs.dev/guide/#scaffolding-your-first-vite-project) देख सकते हैं।

Project बन जाने के बाद हमें Refine dependencies install करनी होंगी।

```sh
npm install @refinedev/core @refinedev/cli
```

हम `@refinedev/core` install कर रहे हैं, जो Refine की सभी core functionalities देता है, और `@refinedev/cli` install कर रहे हैं, जो optional होने के बावजूद development process के लिए कई उपयोगी features देता है। `@refinedev/cli` के बारे में अधिक जानने के लिए आप [इसकी documentation](/core/docs/packages/cli) देख सकते हैं।

### Scripts configure करना

हम अपने `dev`, `build` और `serve` scripts को नीचे दिए गए scripts से बदलेंगे:

```json
{
  "scripts": {
    "dev": "refine dev",
    "build": "refine build",
    "serve": "refine serve"
  }
}
```

`refine` के runner commands bundler द्वारा दिए गए समान commands का उपयोग करेंगे, लेकिन वे dependencies के version checks और Refine team की announcements जैसी उपयोगी सुविधाएं भी देंगे।

### App configure करना

हमें अपने app में `<Refine />` component mount करना होगा। हम इसे app के root पर mount करेंगे।

```tsx title="src/App.tsx"
import { Refine, WelcomePage } from "@refinedev/core";

function App() {
  return (
    <Refine>
      <WelcomePage />
    </Refine>
  );
}

export default App;
```

यहां हम कोई खास काम नहीं कर रहे हैं। हम सिर्फ `<Refine />` component को app में mount कर रहे हैं। `<Refine />` component Refine का core component है और यह app को काम करने के लिए जरूरी context और logic देता है।

`<WelcomePage />` component `@refinedev/core` द्वारा दिया गया component है और यह Refine में आपका स्वागत करने वाला एक simple page है। चाहें तो आप इसे हटा सकते हैं।

इतना app को चलाने के लिए पर्याप्त होगा। अब हम नीचे दिए गए command से app शुरू कर सकते हैं:

```sh
npm run dev
```

जब आप browser खोलकर localhost पर जाएंगे, तो आपको दाईं ओर page दिखना चाहिए। अगर सब कुछ expected तरीके से काम कर रहा है, तो अगले section पर जाएं।

</TabItem>

</Tabs>

:::tip Tailored App Generation

`create-refine-app` default रूप से आपको data providers, authentication, UI libraries आदि चुनने के लिए कुछ steps से गुजारता है, ताकि आपकी जरूरत के अनुसार app बन सके। इसके बारे में आप [quickstart](/core/docs/getting-started/quickstart) section में अधिक पढ़ सकते हैं।

:::

</Sandpack>
