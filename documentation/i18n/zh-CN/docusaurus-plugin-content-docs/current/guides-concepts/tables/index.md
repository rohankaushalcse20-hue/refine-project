---
title: "表格与列表 | Refine v5"
display_title: "表格"
sidebar_label: "表格"
description: "说明如何在 Refine 中构建 tables、lists、filters、sorting 与 pagination。"
---

表格和列表让 API 数据更适合浏览与操作。Refine 已经提供了把 pagination、filters、sorting 和 loading state 连接到 data provider 的 hooks。

## 显示列表

`useTable` 与 `useList` 是最常见的列表入口。你既可以与 UI integrations 搭配使用，也可以接入自定义 components。

```tsx
const table = useTable({
  resource: "products",
  pagination: { pageSize: 10 },
});
```

## 过滤与排序

filters 与 sorters 会被转换为 data provider 可以发送给 API 的参数，从而降低 UI 与 backend 通信细节之间的耦合。

## CRUD actions

你可以在列表中组合 create、edit、show、delete buttons。相关 actions 能遵循 access control provider 的权限判断，labels 也可以通过 i18n 进行翻译。

## 用户体验

应明确处理 loading、empty state 与 error state。面对大数据量表格时，建议结合 pagination 或渐进式加载保持界面响应速度。
