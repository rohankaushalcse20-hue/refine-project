---
title: "通知 | Refine v5"
display_title: "通知"
sidebar_label: "通知"
description: "Refine の notification provider を使って、成功やエラーのメッセージを表示します。"
---

通知は、操作の成功確認やエラー説明に役立ちます。Refine は `notificationProvider` を使って、hooks、mutations、components からメッセージを表示します。

## Notification provider

provider は通常、メッセージを表示する `open` メソッドと、必要に応じて閉じるための `close` メソッドを持ちます。

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

Ant Design、Material UI、Mantine、Chakra UI の統合を使うと、それぞれの通知システムを Refine に接続できます。

## i18n

ローカライズされたアプリでは、成功、失敗、警告のメッセージがユーザーの言語で自然に読めるよう、通知のタイトルや説明も翻訳しましょう。
