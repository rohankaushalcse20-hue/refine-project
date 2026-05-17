<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Airtable 数据提供者示例

这个示例展示如何让 **Refine** 通过 Airtable 读取和管理数据。Refine 的 CRUD hooks 继续调用标准 `dataProvider` 方法，后端请求则由 Airtable 集成完成。

## 本地运行

```bash
npm create refine-app@latest -- --example data-provider-airtable
```

## 建议关注

- Airtable 配置如何映射到 Refine resources
- `dataProvider` 方法和表格字段之间的关系
- 列表、创建和编辑流程的数据流
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 data-provider-airtable 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-airtable?view=preview&theme=dark&codemirror=1)
