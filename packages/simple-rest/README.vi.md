# @refinedev/simple-rest

`@refinedev/simple-rest` cung cấp data provider cho các API REST đơn giản. Package này chuyển các thao tác Refine như `getList`, `getOne`, `create`, `update` và `deleteOne` thành HTTP requests theo quy ước của package.

## Package bao gồm gì?

- Các method `dataProvider` cơ bản cho REST resources.
- Hỗ trợ pagination, sorting và filtering được truyền từ hooks của Refine.
- Điểm bắt đầu gọn cho ví dụ, prototype và API có endpoints dự đoán được.

## Khi nào nên dùng?

Dùng provider này khi backend REST phù hợp với hợp đồng đơn giản hoặc khi bạn muốn chạy nhanh ứng dụng Refine trước khi viết `dataProvider` riêng. Tên methods, endpoints và packages giữ nguyên, không dịch.
