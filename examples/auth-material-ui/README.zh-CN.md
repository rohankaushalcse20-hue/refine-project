<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Material UI 身份验证示例

这个示例展示如何在使用 Material UI 的 **Refine** 应用中构建登录体验。认证逻辑由 Refine 的 provider 处理，界面层则使用 Material UI 组件呈现。

## 本地运行

```bash
npm create refine-app@latest -- --example auth-material-ui
```

## 建议关注

- 登录页面与 Material UI 布局组件的组合
- `authProvider` 如何驱动受保护页面
- 认证状态对导航和资源访问的影响
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 auth-material-ui 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-material-ui?view=preview&theme=dark&codemirror=1)
