---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Kết nối bản dịch và đổi ngôn ngữ thông qua hợp đồng i18nProvider."
slug: /i18n/i18n-provider
---

`i18nProvider` nối Refine với thư viện dịch thuật mà ứng dụng sử dụng. Refine không bắt buộc một giải pháp cụ thể, vì vậy bạn có thể dùng `react-i18next`, `next-intl`, `formatjs` hoặc cơ chế riêng.

## Hợp đồng

Provider thường cung cấp các method `translate`, `changeLocale` và `getLocale`. Nhờ chúng, components của Refine và code ứng dụng có thể lấy văn bản và đổi ngôn ngữ hiện tại một cách nhất quán.

```tsx title=App.tsx
<Refine
  i18nProvider={{
    translate: (key, params) => i18n.t(key, params),
    changeLocale: (lang) => i18n.changeLanguage(lang),
    getLocale: () => i18n.language,
  }}
/>
```

## Khóa bản dịch

Nên dùng khóa ổn định, ví dụ `resources.products.fields.name`. Khóa an toàn hơn dịch theo văn bản nguồn, vì bạn có thể đổi nội dung UI mà không phá hợp đồng component.

## Resources và actions

Bản dịch resource có thể bao gồm nhãn menu, tiêu đề trang, tên field và thông báo action. Nhờ vậy danh sách, form và thông báo cùng dùng một từ điển nghiệp vụ.

## Đổi locale

`changeLocale` nên cập nhật thư viện i18n và, nếu ứng dụng cần, lưu lựa chọn người dùng vào URL, cookie hoặc hồ sơ. Trong ứng dụng Next.js và Remix, lựa chọn locale cũng có thể ảnh hưởng đến routing.

## Gợi ý thực tế

Tách bản dịch nghiệp vụ khỏi văn bản kỹ thuật. Tên API, imports, commands và identifiers nên giữ nguyên, còn phần cần dịch là văn bản hiển thị cho người dùng.
