<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ant Design `useTable` 表格示例

这个示例展示如何在 Ant Design 表格中使用 **Refine** 的 `useTable`。Refine 负责数据查询、分页和排序状态，Ant Design 负责表格展示。

## 本地运行

```bash
npm create refine-app@latest -- --example table-antd-use-table
```

## 建议关注

- `useTable` 返回的 props 如何传给 Ant Design `Table`
- 分页、排序和筛选参数的同步方式
- 列表页面如何围绕 Refine resources 构建
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 table-antd-use-table 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-antd-use-table?view=preview&theme=dark&codemirror=1)
