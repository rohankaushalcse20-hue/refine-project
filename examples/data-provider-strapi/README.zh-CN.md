<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Strapi 数据提供者示例

这个示例展示如何让 **Refine** 与 Strapi API 协同工作。Strapi 提供内容模型和接口，Refine 通过 `dataProvider` 将这些接口接入 CRUD 页面。

## 本地运行

```bash
npm create refine-app@latest -- --example data-provider-strapi
```

## 建议关注

- Strapi API 地址和资源名称的配置方式
- Refine CRUD 操作如何映射到 Strapi 请求
- 列表、编辑和创建页面的数据加载流程
- 原始命令、URL 和 API 名称保持不变

[在 CodeSandbox 中打开 data-provider-strapi 示例](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-strapi?view=preview&theme=dark&codemirror=1)
