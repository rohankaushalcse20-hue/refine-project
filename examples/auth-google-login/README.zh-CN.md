<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Google 登录示例

这个示例展示如何在 **Refine** 应用中接入 Google 登录。它保留 Refine 的认证边界，并把第三方身份验证结果映射到应用可使用的会话状态。

## 本地运行

```bash
npm create refine-app@latest -- --example auth-google-login
```

## 建议关注

- Google 登录按钮与 `authProvider` 的连接方式
- 登录成功后的跳转和会话保存
- Refine 资源访问如何依赖认证状态
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 auth-google-login 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
