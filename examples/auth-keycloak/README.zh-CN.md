<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Keycloak 身份验证示例

这个示例展示如何把 **Refine** 的认证流程接入 Keycloak。Keycloak 负责身份提供与令牌管理，Refine 继续负责资源、路由和应用状态。

## 本地运行

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## 建议关注

- Keycloak 客户端配置与 `authProvider` 的关系
- 登录、登出和权限检查的调用点
- 受保护页面在认证状态变化时的表现
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 auth-keycloak 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
