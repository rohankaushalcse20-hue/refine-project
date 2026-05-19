---
id: serverSideFormValidation
title: "Ví dụ ServerSideFormValidation | Thực hành tốt trong Refine v5"
display_title: "Server-Side Form Validation"
sidebar_label: "Server-Side Form Validation"
description: "Xây dựng ServerSideFormValidation trong Refine v5. Khám phá thực hành tốt cho enterprise UI và component trong bảng quản trị React."
example-tags: [form, antd]
---

Bạn có thể xử lý lỗi server-side form validation mặc định bằng [Ant Design useForm][antd-use-form].

Khi `dataProvider` trả về rejected promise có trường `errors`, [`useForm`][react-hook-form-use-form] sẽ tự động cập nhật trạng thái lỗi bằng trường `errors` bị reject.

[Tham khảo tài liệu server-side Form Validation để biết thêm thông tin. →](/core/docs/guides-concepts/forms/#server-side-validation-)

<CodeSandboxExample path="server-side-form-validation-antd" />

[antd-use-form]: /core/docs/ui-integrations/ant-design/hooks/use-form
[react-hook-form-use-form]: https://react-hook-form.com/api/useform
