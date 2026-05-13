# @refinedev/core

`@refinedev/core` chứa nền tảng headless của Refine. Package này cung cấp component `<Refine />`, hợp đồng providers, data hooks, xử lý resources, mutation modes và các tích hợp cần thiết để xây dựng ứng dụng CRUD độc lập với thư viện UI.

## Package bao gồm gì?

- Cấu hình `resources` cho các action `list`, `create`, `edit`, `show` và `clone`.
- Data hooks như `useList`, `useOne`, `useCreate`, `useUpdate` và `useDelete`.
- Hợp đồng `dataProvider`, `authProvider`, `accessControlProvider`, `notificationProvider`, `i18nProvider` và router provider.
- Cơ chế state, cache và mutations được các tích hợp UI của Refine sử dụng.

## Khi nào nên dùng?

Dùng `@refinedev/core` khi bạn muốn kiểm soát lớp UI riêng hoặc xây dựng tích hợp với thư viện component đã chọn. Tên API, imports và lệnh cài đặt giữ nguyên, không dịch.
