---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Tìm hiểu cách Refine làm việc với router của React, Next.js và Remix."
slug: /guides-concepts/routing
---

Refine không ép buộc một router duy nhất. Thay vào đó, Refine dùng hợp đồng router provider để nối `resources` với navigation, tạo đường dẫn và đọc tham số URL.

## Vai trò của router provider

Router provider cho phép Refine:

- tạo link cho các action `list`, `create`, `edit`, `show` và `clone`;
- đọc tham số như `id` của resource;
- đồng bộ filters, sorting và pagination với URL;
- tích hợp breadcrumbs, menu và chuyển hướng sau mutations.

## Resources và đường dẫn

Đường dẫn khai báo trong `resources` là nguồn sự thật cho navigation. Refine dùng chúng trong hooks và components, nhưng không thay đổi cú pháp router mà ứng dụng đã chọn.

```tsx title=App.tsx
<Refine
  routerProvider={routerProvider}
  resources={[
    {
      name: "orders",
      list: "/orders",
      show: "/orders/:id",
      edit: "/orders/:id/edit",
    },
  ]}
/>
```

## Chọn tích hợp

Trong ứng dụng SPA, React Router là lựa chọn phổ biến. Với ứng dụng render phía server, bạn có thể chọn tích hợp Next.js hoặc Remix. Khái niệm Refine không đổi: `resources` mô tả địa chỉ, còn router provider chuyển chúng sang cơ chế của framework tương ứng.

## Đồng bộ state với URL

Danh sách và bảng có thể lưu filters, sorting và pagination trong URL. Điều này giúp chia sẻ view, quay lại trạng thái trước đó và debug truy vấn. Tính năng này đặc biệt hữu ích trong công cụ nội bộ, nơi người dùng thường quay lại các bộ lọc đã lưu.
