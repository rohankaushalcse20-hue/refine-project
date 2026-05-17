<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ably 实时数据示例

这个示例展示如何把 **Refine** 的实时能力连接到 Ably。页面仍然使用 Refine 的资源和 hooks，实时事件通过 `liveProvider` 更新相关视图。

## 本地运行

```bash
npm create refine-app@latest -- --example live-provider-ably
```

## 建议关注

- Ably client 与 `liveProvider` 的连接方式
- 订阅事件如何刷新列表或详情页
- 实时通道命名与 resources 的关系
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 live-provider-ably 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/live-provider-ably?view=preview&theme=dark&codemirror=1)
