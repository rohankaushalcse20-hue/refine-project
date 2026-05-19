---
id: serverSideFormValidation
title: "ServerSideFormValidation 示例 | Refine v5 最佳实践"
display_title: "Server-Side Form Validation"
sidebar_label: "Server-Side Form Validation"
description: "在 Refine v5 中构建 ServerSideFormValidation。学习关键步骤，探索面向真实 React 管理面板的企业级 UI 和 components 最佳实践。"
example-tags: [form, antd]
---

你可以使用 [Ant Design useForm](/core/docs/ui-integrations/ant-design/hooks/use-form) 开箱即用地处理 server-side form validation errors。

当 `dataProvider` 返回带有 `errors` 字段的 rejected promise 时，[`useForm`](/core/docs/ui-integrations/ant-design/hooks/use-form) 会自动使用被拒绝的 `errors` 字段更新错误状态。

[有关更多信息，请参考 server-side Form Validation 文档。→](/core/docs/guides-concepts/forms/#server-side-validation-)

<CodeSandboxExample path="server-side-form-validation-antd" />
