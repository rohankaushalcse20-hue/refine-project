---
title: "通知 | Refine v5"
display_title: "通知"
sidebar_label: "通知"
description: "通过 Refine 的 notification provider 显示成功、失败与提示消息。"
---

通知适合用来确认操作成功或解释错误原因。Refine 通过 `notificationProvider` 在 hooks、mutations 与 components 中显示消息。

## Notification provider

provider 一般会实现一个用于展示消息的 `open` 方法，以及按需关闭消息的 `close` 方法。

```tsx
const notificationProvider = {
  open: ({ type, message, description }) => {
    console.log(type, message, description);
  },
  close: (key) => {
    console.log("close", key);
  },
};
```

## UI integrations

如果你使用 Ant Design、Material UI、Mantine 或 Chakra UI 集成，就可以直接把这些库自己的通知系统接入 Refine。

## i18n

在本地化应用中，成功、失败和警告消息也应当与界面语言保持一致，因此通知标题与说明文本同样需要翻译。
