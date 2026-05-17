<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Kinde 身份验证示例

这个示例展示如何在 **Refine** 应用中使用 Kinde 处理登录和会话。应用仍然通过 Refine 的 `authProvider` 暴露统一的认证接口。

## 本地运行

```bash
npm create refine-app@latest -- --example auth-kinde
```

## 建议关注

- Kinde 登录流程与 Refine 生命周期的衔接
- 会话信息如何传递给资源页面
- 登出后 routes 和 UI 状态的处理
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 auth-kinde 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
