---
title: "Notifications | Refine v5"
display_title: "Thông báo"
sidebar_label: "Thông báo"
description: "Cấu hình notificationProvider để hiển thị trạng thái thao tác cho người dùng."
slug: /guides-concepts/notifications
---

Thông báo giúp người dùng hiểu kết quả thao tác: lưu thành công, request gặp lỗi hoặc mutation vẫn còn có thể hoàn tác. Trong Refine, phần này do `notificationProvider` phụ trách.

## notificationProvider

Provider cung cấp các method để mở và đóng thông báo. Các tích hợp UI như Ant Design, Material UI, Mantine và Chakra UI có thể nối hệ thống toast, alert hoặc snackbar riêng.

```tsx title=App.tsx
<Refine notificationProvider={notificationProvider} />;
```

## Thông báo tự động

Hooks dữ liệu có thể hiển thị thông báo khi thành công hoặc thất bại. Nhờ vậy create, update và delete có phản hồi cho người dùng mà không phải lặp lại cùng logic ở từng trang.

## Tùy chỉnh nội dung

Nội dung thông báo có thể tùy chỉnh trong options của hooks. Nên viết thông báo theo ngôn ngữ sản phẩm, ví dụ "Đã lưu sản phẩm" thay vì câu kỹ thuật như "Mutation succeeded".

## Lỗi và undoable

Với mutation `undoable`, thông báo có thêm vai trò: cho người dùng cơ hội hoàn tác trước khi thay đổi được gửi bền vững. Với lỗi API, thông báo nên cho biết người dùng có thể thử lại, sửa dữ liệu hay cần liên hệ quản trị viên.

## Bản địa hóa

Trong ứng dụng đa ngôn ngữ, thông báo nên dùng cùng nguồn dịch với phần UI còn lại. `i18nProvider` có thể cung cấp văn bản, còn `notificationProvider` quyết định cách hiển thị chúng.
