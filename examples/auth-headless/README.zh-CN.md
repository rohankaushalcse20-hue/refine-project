<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Headless 身份验证示例

这个示例展示如何在无预设 UI 框架的 **Refine** 应用中实现认证。它突出 Refine 的认证契约，让你可以自由选择自己的页面结构和样式。

## 本地运行

```bash
npm create refine-app@latest -- --example auth-headless
```

## 建议关注

- Headless 场景下 `authProvider` 的最小配置
- 登录、登出和身份检查的调用顺序
- 自定义 UI 如何响应认证状态
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 auth-headless 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-headless?view=preview&theme=dark&codemirror=1)
