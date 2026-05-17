<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Hasura 数据提供者示例

这个示例展示如何在 **Refine** 中使用 Hasura 作为 GraphQL 数据后端。Refine 通过数据提供者发起查询和变更，Hasura 负责 GraphQL schema 与数据访问。

## 本地运行

```bash
npm create refine-app@latest -- --example data-provider-hasura
```

## 建议关注

- Hasura endpoint 与 GraphQL 客户端配置
- Refine 列表和表单 hooks 如何触发查询
- 过滤、排序和分页参数的传递方式
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 data-provider-hasura 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-hasura?view=preview&theme=dark&codemirror=1)
