---
title: "認可 | Refine v5"
display_title: "認可"
sidebar_label: "認可"
description: "access control provider を使って、actions、routes、components へのアクセス権限を制御します。"
---

認可は、認証済みユーザーが何を実行できるかを定義します。Refine では `accessControlProvider` を使い、hooks、buttons、menus、pages から権限を確認できます。

## Access control provider

中心となるメソッドは `can` です。resource、action、追加パラメータを受け取り、その操作を許可するかどうかを判断します。

```tsx
const accessControlProvider = {
  can: async ({ resource, action }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Only admins can delete posts" };
    }

    return { can: true };
  },
};
```

## Components で使う

`useCan` を使うと、権限に応じて UI を切り替えられます。

```tsx
const { data } = useCan({ resource: "posts", action: "delete" });

return data?.can ? <DeleteButton /> : null;
```

## ベストプラクティス

access control provider は UI の体験向上に役立ちますが、最終的な検証は必ず backend 側でも行ってください。
