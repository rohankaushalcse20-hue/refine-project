---
title: "React Router v6 से v7 Migration Guide | Refine v5"
display_title: "Migration Guide from v6 to v7"
description: "Refine v5 में @refinedev/react-router-v6 से @refinedev/react-router और react-router v7 पर migrate करने की Hindi guide।"
sidebar_label: v6 to v7
---

इस guide में हम `@refinedev/react-router-v6` के breaking changes और अपने project को `@refinedev/react-router` के साथ `react-router` v7 पर migrate करने का तरीका cover करेंगे।

> 🚨 Package name changes के अलावा Refine कोई breaking change introduce नहीं करता। फिर भी React Router v7 changes की विस्तृत जानकारी के लिए [React Router v7 migration guide](https://reactrouter.com/upgrading/v6) पढ़ने की सलाह दी जाती है।

## Package Changes

Consistency बनाए रखने और confusion से बचने के लिए package name `@refinedev/react-router-v6` से बदलकर `@refinedev/react-router` किया गया है। साथ ही [version 7](https://reactrouter.com/upgrading/v6#upgrade-to-v7) में `react-router-dom` की जगह `react-router` उपयोग होता है।

सबसे पहले पुराने packages uninstall करें।

```bash
npm uninstall @refinedev/react-router-v6 react-router-dom react-router
```

फिर नए packages install करें।

ध्यान दें कि `react-router-dom` अब आवश्यक नहीं है। सभी react-router v7 components `react-router` package से import किए जाते हैं।

```bash
npm install @refinedev/react-router react-router
```

```diff

- "@refinedev/react-router-v6": "^4.6.0"
+ "@refinedev/react-router": "^1.0.1"

- "react-router-dom": "^6.8.1"
- "react-router": "^6.8.1"
+ "react-router": "^7.0.2"
```

इसके बाद setup तैयार है। अब आप `@refinedev/react-router` को `react-router` v7 के साथ उपयोग करना शुरू कर सकते हैं।

### Imports update करना

Package imports इस तरह बदले गए हैं:

```diff
 import routerProvider, { NavigateToResource, UnsavedChangesNotifier, DocumentTitleHandler }
- from "@refinedev/react-router-v6";
 import routerProvider, { NavigateToResource, UnsavedChangesNotifier, DocumentTitleHandler }
+ from "@refinedev/react-router";

-import { RouterProvider } from "react-router-dom";
+import { RouterProvider } from "react-router";
```

### refine-codemod से imports automatically update करना (recommended)

Imports manually update करने के बजाय, आप `refine-codemod` का उपयोग करके project में imports automatically update कर सकते हैं। ध्यान रखें कि आपका git working tree clean हो, ताकि expected result न मिलने पर आप changes revert कर सकें।

`@refinedev/react-router-v6` से `@refinedev/react-router` के लिए:

```bash
npx @refinedev/codemod@latest refine-react-router-v6-to-refine-react-router
```

`react-router-dom` से `react-router` के लिए:

```bash
npx @refinedev/codemod@latest react-router-dom-to-react-router
```
