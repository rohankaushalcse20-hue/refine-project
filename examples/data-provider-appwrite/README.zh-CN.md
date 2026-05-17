<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Appwrite 数据提供者示例

这个示例展示如何把 **Refine** 的 CRUD 层连接到 Appwrite。应用通过 `dataProvider` 调用 Appwrite 集合，同时保留 Refine 的资源声明和页面流程。

## 本地运行

```bash
npm create refine-app@latest -- --example data-provider-appwrite
```

## 建议关注

- Appwrite project、database 和 collection 的配置位置
- `dataProvider` 如何处理列表、详情和变更
- Refine resources 与 Appwrite 集合的对应关系
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 data-provider-appwrite 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-appwrite?view=preview&theme=dark&codemirror=1)
