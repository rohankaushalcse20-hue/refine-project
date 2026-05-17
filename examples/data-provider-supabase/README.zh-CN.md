<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Supabase 数据提供者示例

这个示例展示如何在 **Refine** 中使用 Supabase 作为数据后端。Refine 的资源页面通过 `dataProvider` 访问 Supabase 表，并保持标准 CRUD 体验。

## 本地运行

```bash
npm create refine-app@latest -- --example data-provider-supabase
```

## 建议关注

- Supabase client 与 `dataProvider` 的初始化方式
- 表名如何对应到 Refine resources
- 查询、筛选和变更在页面中的触发点
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 data-provider-supabase 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-supabase?view=preview&theme=dark&codemirror=1)
