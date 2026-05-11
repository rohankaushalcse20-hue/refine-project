---
title: "Routing गाइड | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Refine में router integrations, route definition और navigation patterns का परिचय।"
---

किसी भी CRUD application में routing केंद्रीय भूमिका निभाता है। Refine की headless architecture आपको किसी एक router तक सीमित नहीं करती, इसलिए आप अपनी पसंद का routing solution चुन सकते हैं।

Refine आधिकारिक रूप से **React Router**, **Next.js** और **Remix** integrations देता है। इन integrations के साथ parameter detection, redirects और navigation helpers का उपयोग आसान हो जाता है।

## Router provider कैसे जोड़ें

Refine में routing enable करने के लिए चुना गया router integration import करें और उसे `<Refine />` के `routerProvider` prop में pass करें।

```tsx title="App.tsx"
import { BrowserRouter, Routes } from "react-router";
import routerProvider from "@refinedev/react-router";

const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* Your route definitions */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

## क्या लाभ मिलते हैं

- hooks और components में route parameters का बेहतर integration
- mutation और auth flows के बाद automatic redirects
- breadcrumbs और links जैसी navigation utilities

## ध्यान रखने वाली बात

Refine router-agnostic है, इसलिए actual route tree आपकी जिम्मेदारी रहती है। React Router में `Routes`, Next.js में `pages` या `app`, और Remix में `app/routes` structure define करना आपको ही करना होगा।
