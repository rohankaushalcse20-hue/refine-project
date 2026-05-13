---
title: "Overview | Refine v5"
display_title: "Tổng quan"
sidebar_label: "Tổng quan"
description: "Tìm hiểu ý tưởng của Refine trước khi xây dựng ứng dụng React tập trung vào CRUD."
displayed_sidebar: mainSidebar
slug: /getting-started/overview
---

**Refine** là framework headless để xây dựng nhanh các ứng dụng React giàu dữ liệu. Refine gom các nhu cầu quen thuộc của admin panel, công cụ nội bộ, dashboard, cổng B2B và luồng CRUD vào một kiến trúc thống nhất: đọc dữ liệu, biểu mẫu, bảng, routing, authentication và authorization.

Refine vẫn để bạn kiểm soát lớp UI. Bạn có thể dùng Ant Design, Material UI, Mantine, Chakra UI, Tailwind CSS hoặc design system riêng. Bạn cũng có thể chạy hoàn toàn headless với `@refinedev/core`.

## Vì sao chọn Refine?

- **Headless core:** hành vi dữ liệu, state và navigation không bị khóa vào một framework UI.
- **Kiến trúc provider:** `dataProvider`, `authProvider`, `accessControlProvider`, `notificationProvider`, `i18nProvider` và router provider giúp thay thế từng phần tích hợp của ứng dụng.
- **Năng suất CRUD:** cung cấp các mẫu chung cho những thao tác như `list`, `show`, `create`, `edit` và `clone`.
- **Tình huống thực tế:** hỗ trợ filtering, pagination, optimistic updates, realtime, audit logs và multi-tenancy.

## Cấu trúc cơ bản

Ứng dụng Refine thường được mô hình hóa quanh `resources` và `providers`. `resources` mô tả các thực thể miền nghiệp vụ, còn `providers` kết nối ứng dụng với dữ liệu, xác thực, thông báo và routing.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        create: "/products/new",
        edit: "/products/:id/edit",
        show: "/products/:id",
      },
    ]}
  />
);
```

## Bước tiếp theo

Để tạo dự án mới, hãy xem [Quickstart](/core/docs/getting-started/quickstart/). Để hiểu rõ kiến trúc hơn, bắt đầu với [General Concepts](/core/docs/guides-concepts/general-concepts/) và [Data Fetching](/core/docs/guides-concepts/data-fetching/).
