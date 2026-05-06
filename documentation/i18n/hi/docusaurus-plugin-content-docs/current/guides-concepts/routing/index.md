---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "React Router, Next.js, Remix या किसी compatible system के साथ Refine routing सेट करें।"
---

Routing किसी भी CRUD application के लिए ज़रूरी है। Refine की headless architecture आपको किसी एक framework या router तक सीमित किए बिना अपनी पसंद का routing solution चुनने देती है।

Refine **React Router**, **Next.js** और **Remix** के लिए built-in integrations देता है। ये integrations parameters को automatically detect करने, mutations या authentication के बाद redirects संभालने और navigation utilities उपयोग करने में मदद करती हैं।

Refine router agnostic रहता है, इसलिए routes की परिभाषा आपको ही करनी होती है: React Router में `Routes`, Next.js में `pages` या `app`, और Remix में `app/routes`.

## Router provider जोड़ना

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Routes } from "react-router";

export const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* आपके routes */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

Routes और resources को एक-दूसरे के अनुरूप रखें, ताकि `resource`, `id` और दूसरे parameters route से infer किए जा सकें।
