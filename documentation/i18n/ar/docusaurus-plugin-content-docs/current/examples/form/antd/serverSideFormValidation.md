---
id: serverSideFormValidation
title: "مثال ServerSideFormValidation | أفضل الممارسات في Refine v5"
display_title: "Server-Side Form Validation"
sidebar_label: "Server-Side Form Validation"
description: "ابنِ ServerSideFormValidation في Refine v5 وتعلّم الخطوات الأساسية وأفضل ممارسات واجهات المؤسسة والمكوّنات للوحات React إدارية."
example-tags: [form, antd]
---

يمكنك التعامل مع أخطاء التحقق من النماذج في الخادم مباشرة باستخدام [Ant Design useForm][antd-use-form].

عندما يعيد `dataProvider` وعداً مرفوضاً يحتوي على حقل `errors`، سيحدّث `useForm` حالة الخطأ تلقائياً باستخدام حقل `errors` المرفوض.

[راجع توثيق server-side Form Validation لمزيد من المعلومات. →](/core/docs/guides-concepts/forms/#server-side-validation-)

<CodeSandboxExample path="server-side-form-validation-antd" />

[antd-use-form]: /core/docs/ui-integrations/ant-design/hooks/use-form
