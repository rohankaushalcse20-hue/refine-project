---
title: "表单 | Refine v5"
display_title: "表单"
sidebar_label: "表单"
description: "结合 Refine、UI integrations 与服务端校验构建 CRUD 表单。"
---

表单是 CRUD 应用中的核心交互。Refine 提供了将字段、data providers、validation 与 mutations 串联起来的 hooks 与 components。

## 基本方式

你可以接入 Ant Design、Material UI、Mantine、Chakra UI 或 React Hook Form。Refine 的逻辑与展示层解耦，因此可以自由选择符合产品要求的 UI 库。

## 创建与编辑

借助 `useForm`、`useModalForm`、`useDrawerForm`、`useStepsForm` 等 hooks，可以组织创建、编辑或多步骤表单流程。

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
});
```

## Select 与关联数据

`useSelect` 能从 resource 获取 options，便于处理关联字段、filters 和远程搜索。

## 校验

可以同时使用本地校验和服务端返回的错误。在多语言应用中，建议让错误文案保持清晰，并通过 i18n provider 统一翻译。
