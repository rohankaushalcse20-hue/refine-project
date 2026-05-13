---
title: "Authentication | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "Cấu hình authProvider để xử lý đăng nhập, đăng xuất và kiểm tra phiên trong Refine."
slug: /guides-concepts/authentication
---

Authentication trong Refine được xử lý bởi `authProvider`. Nhờ vậy ứng dụng có thể dùng bất kỳ cơ chế định danh nào: API riêng, Auth0, Keycloak, Google, Azure AD hoặc nhà cung cấp khác.

## Nhiệm vụ của authProvider

`authProvider` thường triển khai các method:

- `login` để bắt đầu phiên người dùng;
- `logout` để kết thúc phiên;
- `check` để kiểm tra người dùng còn đăng nhập hay không;
- `getIdentity` để lấy dữ liệu hồ sơ;
- `onError` để phản ứng với lỗi API, chẳng hạn token hết hạn.

## Bảo vệ route

Kết hợp `authProvider` với router provider cho phép bảo vệ các trang create, edit, show và list. Khi `check` trả về trạng thái không có quyền, ứng dụng có thể chuyển người dùng đến trang đăng nhập.

```tsx title=App.tsx
<Refine
  authProvider={authProvider}
  resources={[
    {
      name: "posts",
      list: "/posts",
    },
  ]}
/>
```

## Tokens và phiên

Refine không áp đặt nơi lưu token. Bạn có thể dùng cookies, storage của trình duyệt hoặc session phía server. Điều quan trọng là `dataProvider` và `authProvider` phải dùng cùng nguồn thông tin về phiên hiện tại.

## Trải nghiệm người dùng

Authentication tốt cần xử lý rõ trạng thái loading, phiên hết hạn và lỗi đăng nhập. `notificationProvider` có thể hiển thị thông báo, còn `getIdentity` có thể cấp tên, email hoặc vai trò cho UI.
