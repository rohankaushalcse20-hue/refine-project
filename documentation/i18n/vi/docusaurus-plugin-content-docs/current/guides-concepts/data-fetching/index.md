---
title: "Data Fetching | Refine v5"
display_title: "Lấy dữ liệu"
sidebar_label: "Lấy dữ liệu"
description: "Xem cách Refine dùng data providers và hooks để làm việc với API."
slug: /guides-concepts/data-fetching
---

Lấy dữ liệu trong Refine dựa trên hợp đồng `dataProvider`. Hợp đồng này tách logic ứng dụng khỏi API cụ thể, nhờ đó cùng một hook có thể hoạt động với REST, GraphQL, Supabase, Strapi, Hasura hoặc backend riêng.

## Data provider

`dataProvider` triển khai các method như `getList`, `getOne`, `create`, `update`, `deleteOne`, `getMany` và `custom`. Refine gọi chúng dựa trên resource, action và tham số được truyền vào hooks.

```tsx title=App.tsx
import dataProvider from "@refinedev/simple-rest";

<Refine dataProvider={dataProvider("https://api.fake-rest.refine.dev")} />;
```

## Hooks dữ liệu

Các hook thường dùng gồm:

- `useList` để lấy collection;
- `useOne` để lấy một record;
- `useCreate`, `useUpdate` và `useDelete` cho mutations;
- `useTable` để nối danh sách với pagination, sorting và filtering;
- `useForm` để xử lý form create và edit.

## Tham số truy vấn

Hooks truyền thông tin pagination, sorting, filters và `meta` cho `dataProvider`. Nhờ vậy provider có thể xây dựng HTTP request hoặc GraphQL query phù hợp mà không cần thay đổi component UI.

## Xử lý lỗi

Lỗi từ `dataProvider` được trả về hooks và có thể hiển thị qua `notificationProvider`. Trong ứng dụng production, nên chuẩn hóa lỗi backend để components nhận được định dạng dự đoán được.

## Nhiều nguồn dữ liệu

Refine có thể dùng nhiều data providers trong cùng một ứng dụng. Điều này hữu ích khi admin panel kết nối API nội bộ, dịch vụ tìm kiếm và hệ thống billing bên ngoài.
