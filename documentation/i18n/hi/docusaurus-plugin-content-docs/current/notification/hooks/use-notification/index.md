---
title: "useNotification Hook | Refine v5"
display_title: "useNotification"
sidebar_label: "useNotification"
description: "Refine v5 में notificationProvider के open और close methods के लिए useNotification hook का Hindi परिचय।"
source: https://github.com/refinedev/refine/blob/main/packages/core/src/hooks/notification/useNotification/index.ts
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import BasicUsageLivePreview from "./basic-usage-live-preview.md";

`useNotification` का उपयोग किसी भी समय notification को `open` या `close` करने के लिए किया जा सकता है। यह अंदरूनी रूप से [`notificationProvider`](/core/docs/notification/notification-provider/) के `open` और `close` methods लौटाता है।

## Usage

नीचे `useNotification` hook के उपयोग का एक बुनियादी example दिया गया है।

 <BasicUsageLivePreview/>

## Properties

### open

इस method को call करके आप नया notification box खोल सकते हैं।

```tsx
const { open } = useNotification();

open?.({
  type: "success",
  message: "Success",
  description: "This is a success message",
});
```

> अधिक जानकारी के लिए [`Open Notification Params` interface →](/core/docs/core/interface-references#open-notification-params) देखें।

### close

आप `key` की मदद से notification को close कर सकते हैं।

```tsx
const { close } = useNotification();

close?.("notification-key");
```

`open` method में `key` देना जरूरी है। इसी key का उपयोग notification को बंद करने के लिए किया जाता है।

## FAQ

### undoable notification कैसे उपयोग करें?

Undoable notifications दिखाने के लिए `type=progress` होना चाहिए। इसके बाद एक function trigger किया जा सकता है।

```tsx
const { open } = useNotification();

open?.({
  type: "progress",
  message: "Progress",
  undoableTimeout: 5,
  cancelMutation: () => {
    // when undo button is clicked, run this callback
  },
});
```

## API Reference

### Return Values

| Property | Description               | Type                                                                                        |
| -------- | ------------------------- | ------------------------------------------------------------------------------------------- |
| open     | Open Notification Params  | [`Open Notification Params`](/core/docs/core/interface-references#open-notification-params) |
| close    | Close Notification Params | `(key: string) => void;`                                                                    |
