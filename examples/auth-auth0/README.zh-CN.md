<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Auth0 身份验证示例

这个示例展示如何把 **Refine** 连接到 Auth0 登录流程。Refine 的 resources、routes 和 providers 结构保持不变，用户身份与会话处理交给 Auth0 完成。

## 本地运行

```bash
npm create refine-app@latest -- --example auth-auth0
```

## 建议关注

- Auth0 与 `authProvider` 的集成方式
- 已登录 routes 和 resources 的保护流程
- 外部登录回调如何回到 Refine 应用
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 auth-auth0 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
