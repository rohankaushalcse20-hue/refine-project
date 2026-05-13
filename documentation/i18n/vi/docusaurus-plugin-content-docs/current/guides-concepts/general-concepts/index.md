---
title: "General Concepts | Refine v5"
display_title: "Khái niệm chung"
sidebar_label: "Khái niệm chung"
description: "Tìm hiểu các phần cốt lõi trong kiến trúc Refine: resources, providers, hooks và mutation modes."
slug: /guides-concepts/general-concepts
---

Refine tổ chức ứng dụng quanh một vài hợp đồng ổn định. Quan trọng nhất là `resources`, providers và hooks, giúp mô tả logic CRUD mà không gắn chặt với một thư viện UI cụ thể.

## Resources

`resources` mô tả các thực thể miền nghiệp vụ của ứng dụng. Mỗi resource có thể có đường dẫn `list`, `create`, `edit`, `show` và `clone`, cùng metadata dùng cho menu, breadcrumbs và quyền truy cập.

```tsx title=App.tsx
<Refine
  resources={[
    {
      name: "products",
      list: "/products",
      create: "/products/new",
      edit: "/products/:id/edit",
      show: "/products/:id",
      meta: {
        canDelete: true,
      },
    },
  ]}
/>
```

## Providers

Providers là ranh giới giữa Refine và dịch vụ bên ngoài. `dataProvider` giao tiếp với API, `authProvider` xử lý authentication, `accessControlProvider` phụ trách authorization, còn `notificationProvider` hiển thị thông báo cho người dùng.

## Hooks

Các hook của Refine như `useList`, `useOne`, `useCreate`, `useUpdate`, `useTable` và `useForm` dùng providers và resources. Nhờ vậy logic dữ liệu giữ nguyên dù UI được xây bằng Material UI, Ant Design, Mantine, Chakra UI hay component riêng.

## Mutation modes

Refine hỗ trợ nhiều chế độ mutation. `pessimistic` chờ phản hồi từ server, `optimistic` cập nhật UI ngay lập tức, còn `undoable` cho người dùng một khoảng ngắn để hoàn tác thao tác. Lựa chọn chế độ phụ thuộc vào rủi ro dữ liệu và trải nghiệm mong muốn.

## Tiếp theo

Sau khi nắm các thành phần này, hãy đọc [Routing](/core/docs/guides-concepts/routing/) và [Data Fetching](/core/docs/guides-concepts/data-fetching/), nơi các hợp đồng tương tự được áp dụng trong thực tế.
