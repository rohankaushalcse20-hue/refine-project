---
title: "Notifications गाइड | Refine v5"
display_title: "Notifications"
sidebar_label: "Notifications"
description: "Refine notificationProvider, automatic feedback और undoable flows का Hindi summary।"
---

Notifications application में visual feedback देने का महत्वपूर्ण हिस्सा हैं। Refine data operations और auth flows के दौरान success, error और progress feedback दिखाने के लिए built-in notification integration देता है।

## Notification Provider

Notification system enable करने के लिए `<Refine />` को `notificationProvider` दिया जाता है। इसमें सामान्यतः `open` और `close` methods होते हैं।

```ts
interface NotificationProvider {
  open: (params: OpenNotificationParams) => void;
  close: (key: string) => void;
}
```

## Refine इसे कहां उपयोग करता है

- form submission success या error
- create, update, delete, import और export actions
- failed data fetching
- login, logout, register और password flows

## Built-in integrations

Ant Design, Material UI, Mantine और Chakra UI के notification systems को `notificationProvider` के रूप में इस्तेमाल किया जा सकता है ताकि app का design language consistent रहे।

## Undoable notifications

Refine `progress` type के साथ undoable notifications भी support करता है। यह mutation को timeout window में cancel करने के लिए उपयोगी है।
