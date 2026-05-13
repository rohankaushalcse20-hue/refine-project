---
title: "Forms | Refine v5"
display_title: "Biểu mẫu"
sidebar_label: "Biểu mẫu"
description: "Xây dựng form create và edit bằng hooks của Refine cùng thư viện UI đã chọn."
slug: /guides-concepts/forms
---

Biểu mẫu trong Refine nối logic dữ liệu với thư viện UI. Các hook như `useForm` chuẩn bị thao tác lưu, validation phía server và chuyển hướng, còn component UI phụ trách cách hiển thị trường nhập.

## useForm

`useForm` là hook thường dùng nhất cho trang create và edit. Hook này dùng `dataProvider` để chạy `create` hoặc `update`, đồng thời dùng router provider để chuyển đến view phù hợp sau khi lưu.

```tsx title=CreatePage.tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "create",
});
```

## Thư viện UI

Refine cung cấp tích hợp form cho Ant Design, Material UI, Mantine, Chakra UI và React Hook Form. Ở chế độ headless, bạn có thể dùng `@refinedev/core` và nối component riêng mà không đổi hợp đồng dữ liệu.

## Validation

Validation có thể chạy ở client, server hoặc cả hai. Khi backend trả lỗi trường, nên ánh xạ lỗi sang cấu trúc mà thư viện form đã chọn mong đợi để người dùng thấy thông báo đúng cạnh trường tương ứng.

## Quan hệ và select

Các hook như `useSelect` giúp cấp dữ liệu từ resource khác cho field chọn. Đây là trường hợp thường gặp khi form cho phép chọn danh mục, chủ sở hữu, trạng thái hoặc record liên quan.

## Luồng lưu

Sau khi lưu thành công, bạn có thể ở lại trang, chuyển về danh sách, hiển thị view `show` hoặc tiếp tục chỉnh sửa. Hành vi này phụ thuộc yêu cầu sản phẩm và có thể cấu hình trong options của hook.
