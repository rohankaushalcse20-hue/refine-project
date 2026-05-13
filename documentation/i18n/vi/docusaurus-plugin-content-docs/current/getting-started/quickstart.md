---
title: "Quickstart | Refine v5"
display_title: "Quickstart"
sidebar_label: "Quickstart"
description: "Tạo ứng dụng Refine đầu tiên và chạy cục bộ."
displayed_sidebar: mainSidebar
slug: /getting-started/quickstart
---

Quickstart này hướng dẫn bạn tạo một ứng dụng Refine mới, chọn tích hợp UI và chạy dev server. Lệnh terminal và tên package giữ nguyên như tài liệu tiếng Anh.

## Tạo dự án

Cách đơn giản nhất là dùng `create refine-app`:

```sh
npm create refine-app@latest
```

Trình tạo sẽ hỏi về framework, thư viện UI, data provider và các tính năng tùy chọn. Với ứng dụng đầu tiên, bạn có thể chọn cấu hình Vite, React và `@refinedev/simple-rest`, sau đó thay provider bằng tích hợp riêng khi cần.

## Chạy ứng dụng

Sau khi tạo dự án, chuyển vào thư mục ứng dụng và chạy dev server:

```sh
npm run dev
```

Refine sẽ render ứng dụng với component `<Refine />`, resources và providers do template cấu hình. Tùy thư viện UI đã chọn, bạn sẽ thấy các trang list, create, edit và show có sẵn.

## Nên kiểm tra gì?

- File `src/App.tsx`, nơi cấu hình `resources` và providers.
- `dataProvider` đã chọn, thành phần ánh xạ truy vấn Refine sang API.
- Các trang resource dùng hook như `useTable`, `useForm`, `useList` và `useOne`.
- Cấu hình routing nếu dự án dùng React Router, Next.js hoặc Remix.

## Bước tiếp theo

Khi ứng dụng đã chạy cục bộ, hãy đọc [General Concepts](/core/docs/guides-concepts/general-concepts/) để nắm mô hình `resources`, rồi đọc [Data Fetching](/core/docs/guides-concepts/data-fetching/) để hiểu hợp đồng `dataProvider`.
