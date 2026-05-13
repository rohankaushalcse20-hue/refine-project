---
title: "Tables | Refine v5"
display_title: "Bảng"
sidebar_label: "Bảng"
description: "Tạo danh sách và bảng dữ liệu với pagination, sorting và filters."
slug: /guides-concepts/tables
---

Bảng là một trong những view phổ biến nhất trong ứng dụng CRUD. Refine cung cấp hooks nối `dataProvider` với thư viện UI và giúp xử lý pagination, sorting, filters cũng như đồng bộ với URL.

## useTable

`useTable` xây dựng lớp dữ liệu cho bảng. Hook lấy records qua `dataProvider.getList`, truyền tham số pagination và sorting, rồi trả về props cần thiết cho tích hợp UI đã chọn.

```tsx title=ListPage.tsx
const { tableProps } = useTable({
  resource: "products",
  syncWithLocation: true,
});
```

## Filtering và sorting

Filters và sorters được truyền cho `dataProvider` bằng định dạng dự đoán được. Provider quyết định cách chuyển chúng thành tham số REST, GraphQL query hoặc cú pháp backend cụ thể.

## Đồng bộ với địa chỉ

`syncWithLocation` lưu state của bảng trong URL. Nhờ vậy người dùng có thể chia sẻ link tới danh sách với trang, bộ lọc và thứ tự sắp xếp cụ thể, rồi sau khi refresh vẫn quay lại cùng view.

## Action trên dòng

Các action dòng thường gặp là `show`, `edit`, `clone` và `delete`. Refine dùng cấu hình `resources` để tạo đường dẫn phù hợp và kiểm tra quyền qua `accessControlProvider`.

## Hiệu năng

Với tập dữ liệu lớn, hãy filter, sort và paginate ở phía server. Bảng chỉ nên hiển thị phần dữ liệu cần thiết, còn `dataProvider` nên trả cả tổng số records nếu UI yêu cầu.
