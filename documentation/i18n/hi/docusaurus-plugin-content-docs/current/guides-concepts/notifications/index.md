---
title: "Notifications | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "Refine notification provider के माध्यम से success और error messages दिखाएँ।"
---

Notifications users को actions के परिणाम और errors दोनों समझाने में मदद करती हैं। Refine `notificationProvider` के ज़रिए hooks, mutations और components से messages दिखाता है।

## Notification provider

आमतौर पर provider `open` और कभी-कभी `close` methods देता है।

```tsx
const notificationProvider = {
  open: ({ type, message, description }) => {
    console.log(type, message, description);
  },
  close: (key) => console.log("close", key),
};
```

Ant Design, Material UI, Mantine और Chakra UI जैसी integrations अपनी notification systems को Refine से जोड़ सकती हैं।

Localized app में titles और descriptions का translation करें, ताकि feedback target audience के लिए स्पष्ट रहे।
