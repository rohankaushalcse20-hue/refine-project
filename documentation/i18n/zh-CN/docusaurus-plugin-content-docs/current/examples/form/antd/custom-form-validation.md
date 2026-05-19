---
id: custom-form-validation
title: "Custom Form Validation 示例 | Refine v5 中的企业级 UI"
display_title: "Custom Form Validation"
sidebar_label: "Custom Form Validation"
description: "在 Refine v5 中设置 Custom Form Validation。学习最佳实践，探索面向真实 React 管理面板的 provider，并包含实操示例。"
example-tags: [form, antd]
---

你可以通过 Ant Design [Form.Item](https://ant.design/components/form/#Form.Item) 的 rules 属性，为使用 Refine 创建的表单添加基础校验。此外，它也允许你根据需求添加自定义校验。通过在 Form.Item rules 属性中使用 validator 函数，可以很容易地添加自己的规则和校验。下面的示例会详细说明 custom form validation 流程。

[有关更多信息，请参考 Refine Custom Form Validation 文档。→](/core/docs/ui-integrations/ant-design/hooks/use-steps-form/)

<CodeSandboxExample path="form-antd-custom-validation" />
