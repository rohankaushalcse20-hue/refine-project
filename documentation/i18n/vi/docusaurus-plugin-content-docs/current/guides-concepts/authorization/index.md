---
title: "Authorization | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "Dùng accessControlProvider để kiểm soát quyền truy cập resource và action."
slug: /guides-concepts/authorization
---

Authorization xác định người dùng đã đăng nhập được phép làm gì trong ứng dụng. Trong Refine, phần này do `accessControlProvider` đảm nhiệm bằng cách kiểm tra quyền cho resource, action và các tham số tùy chọn.

## accessControlProvider

Method quan trọng nhất là `can`. Method này nhận thông tin về action, resource và `params`, rồi trả về quyết định thao tác có được phép hay không.

```tsx title=App.tsx
<Refine
  accessControlProvider={{
    can: async ({ resource, action }) => {
      return { can: resource === "posts" && action === "list" };
    },
  }}
/>
```

## Actions và resources

Các action phổ biến là `list`, `create`, `edit`, `show`, `delete` và các thao tác nghiệp vụ riêng. Resource lấy từ cấu hình `resources`, vì vậy nên giữ tên nhất quán giữa routing, data provider và authorization.

## Ẩn UI

Authorization không chỉ ảnh hưởng đến quyền vào trang. Nó còn có thể ẩn nút create, edit và delete, chặn menu item hoặc thay đổi khả năng hiển thị trường trong form. Tuy nhiên UI chỉ nên xem đây là tiện ích cho người dùng, không phải lớp bảo mật duy nhất.

## Tích hợp backend

Trong ứng dụng production, quyết định cuối cùng phải được thực thi ở API. `accessControlProvider` có thể dùng vai trò người dùng, claims trong token, phản hồi backend hoặc hệ thống policy bên ngoài như Casbin, Cerbos hay Permify.

## Thực hành tốt

Giữ rule authorization gần model nghiệp vụ. Khi rule phụ thuộc vào chủ sở hữu record, tổ chức hoặc tenant ID, hãy truyền dữ liệu cần thiết qua `params` để quyết định rõ ràng và dễ kiểm thử.
